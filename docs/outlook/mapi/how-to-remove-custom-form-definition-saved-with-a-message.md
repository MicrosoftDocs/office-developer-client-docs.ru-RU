---
title: Удаление определения настраиваемой формы, сохраненного с сообщением
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408469"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Удаление определения настраиваемой формы, сохраненного с сообщением
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе показан пример кода на языке C++, который преобразует сообщение, сохраненное с настраиваемым определением формы, в обычное сообщение без определения формы.
  
В Microsoft Outlook 2010 или Microsoft Outlook 2013 можно совместно использовать формы, содержащие настраиваемые страницы форм, либо опубликовав их в библиотеке форм, либо сохраняя соответствующее определение формы с сообщением. Настраиваемая форма, сохраненная с сообщением, обычно называется "одноразовой формой", так как эта форма доступна только для просмотра определенного сообщения в качестве одноразового экземпляра. Это обычно делается, когда форма не публикуется в библиотеке форм, но вы хотите, чтобы получатель использовал настраиваемую форму при открытии элемента. Вы можете указать форму в качестве одноразовой в конструкторе форм, установив флажок **Отправить определение формы с элементом** на странице **свойств** формы. 
  
Формы, содержащие страницы форм, можно изменять с помощью кода в Visual Basic Scripting Edition (VBScript). Сообщения, сохраненные с определениями форм, обычно имеют больший размер. В целях обеспечения безопасности и хранения Outlook 2010 и Outlook 2013 игнорируют определения форм, сохраненные с любым элементом.
  
Чтобы преобразовать сообщение, сохраненное с настраиваемым определением формы, на одно без, необходимо удалить четыре именованных свойства:
  
- [������������ �������� PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [������������ �������� PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [������������ �������� PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [������������ �������� PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Кроме того, следует удалить [каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) , которое содержит определения настраиваемых свойств, сохраненных с этим сообщением. Побочным результатом удаления этого свойства является то, что объектные модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получать доступ к свойствам пользователей, которые были заданы для сообщения. Вы по-прежнему можете получать доступ к этим свойствам и их значениям с помощью MAPI. Обратите внимание, что если не удалить это свойство, а сообщение сохранено с другим определением формы, [каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично перезаписывается новыми данными, а целостность данных не гарантируется. 
  
Если удалить [каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), необходимо также удалить флаг **INSP_PROPDEFINITION** из [каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
Приведенная ниже функция `RemoveOneOff`принимает указатель на сообщение в качестве входных параметров и определяет, следует ли удалить [каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). С помощью указателя сообщения вызывается метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить соответствующие идентификаторы свойств, а затем вызывает [IMAPIProp::D елетепропс](imapiprop-deleteprops.md) для удаления именованных свойств. Кроме того, он вызывает [IMAPIProp:: PROPS](imapiprop-getprops.md) , чтобы получить [каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md) , и снимает флажок **инсп\_онеофффлагс** и **поINSP_PROPDEFINITIONный** флаг в соответствии с этим свойством, чтобы Outlook 2010 и Outlook 2013 не выполнял поиск таких именованных свойств, которые были удалены. 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a>См. также

- [Константы MAPI](mapi-constants.md)

