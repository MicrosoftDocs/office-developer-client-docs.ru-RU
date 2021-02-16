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
  
В этом разделе показан пример кода на C++, который преобразует сообщение, сохраненное с помощью пользовательского определения формы, в обычное сообщение без определения формы.
  
В Microsoft Outlook 2010, русская версия Или Microsoft Outlook 2013 можно совместно использовать формы, содержащие настраиваемые страницы форм, публикуя их в библиотеке форм или сохранения соответствующего определения формы в сообщении. Настраиваемая форма, сохраненная в сообщении, обычно называется "одноавъемной формой", так как она используется только для просмотра конкретного сообщения как разовой формы. Обычно это происходит, когда форма не публикуется в библиотеке форм, но необходимо, чтобы получатель мог использовать настраиваемую форму при открытии элемента. Вы можете указать, что форма является односетной в  конструкторе форм, выбрав  определение формы отправки с помощью элемента на странице "Свойства" формы. 
  
Формы, содержащие страницы форм, можно настроить с помощью кода в Visual Basic Scripting Edition (VBScript). Как правило, размер сообщений, сохраненных с определениями форм, больше. Из соображений безопасности и хранения Outlook 2010 и Outlook 2013 игнорируют определения форм, сохраненные с любым элементом.
  
Чтобы преобразовать сообщение, сохраненное с пользовательским определением формы, в одно без него, необходимо удалить четыре именуемые свойства:
  
- [������������ �������� PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [������������ �������� PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [������������ �������� PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [������������ �������� PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Кроме того, необходимо удалить каноническое свойство [PidLidPropertyDefinitionStream,](pidlidpropertydefinitionstream-canonical-property.md) которое содержит определения пользовательских свойств, сохраненных в этом сообщении. Побочным эффектом удаления этого свойства является то, что объектные модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получить доступ к свойствам пользователей, заданной для сообщения. Вы по-прежнему можете получить доступ к этим свойствам и их значениям с помощью MAPI. Обратите внимание, что если это свойство не удаляется и сообщение сохранено с помощью другого определения формы, каноническое свойство [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично перезаписывается новыми данными, а целостность данных не гарантируется. 
  
Если удалить каноническое свойство [PidLidPropertyDefinitionStream,](pidlidpropertydefinitionstream-canonical-property.md)следует также удалить флаг **INSP_PROPDEFINITION** из канонического свойства [PidLidCustomFlag.](pidlidcustomflag-canonical-property.md)
  
Следующая функция, принимает в качестве входных параметров указатель на сообщение и индикатор удаления канонического свойства `RemoveOneOff` [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md) С помощью указателя сообщения он вызывает [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения соответствующих идентификаторов свойств, а затем вызывает [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) для удаления именуемой свойства. Он также вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения канонического свойства [PidLidCustomFlag](pidlidcustomflag-canonical-property.md) и удаляет флаг **INSP \_ ONEOFFFLAGS** и **флаг INSP_PROPDEFINITION** соответствующим образом из этого свойства, чтобы Outlook 2010 и Outlook 2013 не искать те именовались свойства, которые были удалены. 
  
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

