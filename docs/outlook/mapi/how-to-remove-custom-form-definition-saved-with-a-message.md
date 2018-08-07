---
title: Удалите Определение настраиваемой формы, сохраненных в сообщение
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 9581656c40af39338f8919903f6d0de29c20a061
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808631"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Удалите Определение настраиваемой формы, сохраненных в сообщение
  
**Относится к**: Outlook 
  
В этом разделе приводится пример кода c++, который преобразует сообщения, который был сохранен с определениями настраиваемых форм для регулярного сообщение без определения формы.
  
В Microsoft Outlook 2010 или Microsoft Outlook 2013 совместное использование форм, содержащих настраиваемые страницы форм по их публикации в библиотеке форм или сохранения соответствующее определение формы с сообщением. Настраиваемая форма, сохраненных в сообщение режимами «одноразовых формы,» с момента формы совместно используется только для просмотра отдельного сообщения как одноразовых экземпляр. Обычно это делается при формы не публикуется в библиотеке форм, но разрешить получателю использовать настраиваемую форму при открытии элемента. Можно указать, что формы — одного раза в конструкторе форм, установив флажок **Отправлять вместе с элементом** на странице **свойств** формы. 
  
Форм, содержащих страниц форм можно настроить с помощью кода в Visual Basic Scripting Edition (VBScript). Сообщения, которые будут сохранены с определения формы, обычно больше по размеру. Для безопасности и для обеспечения хранения Outlook 2010 и Outlook 2013 игнорировать определения форм, сохраненных в любой элемент.
  
Чтобы преобразовать сообщение, в котором сохраняется с определениями настраиваемых форм к одному без, необходимо удалить четыре именованных свойств:
  
- [������������ �������� PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [������������ �������� PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [������������ �������� PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [������������ �������� PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Кроме того следует удалить [PidLidPropertyDefinitionStream каноническое свойство](pidlidpropertydefinitionstream-canonical-property.md) , которое содержит определения пользовательских свойств, сохраненных в этого сообщения. Влияние со стороны удаления это свойство является то, что объектной модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получать доступ к свойствам пользователя, которые были установлены в окне сообщения. По-прежнему можно получить доступ к эти свойства и их значения через MAPI. Обратите внимание, что если это свойство не удаляйте и сообщение сохраняется с другой определение формы, [Свойство каноническое PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично заменены новыми данными и целостность данных не гарантируется. 
  
При удалении [Каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)также удалите флаг **INSP_PROPDEFINITION** из [PidLidCustomFlag каноническое свойство](pidlidcustomflag-canonical-property.md).
  
Следующая функция `RemoveOneOff`, принимает в качестве входных параметров указатель на сообщение и индикатор необходимость удаления [Каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). С помощью указателя мыши сообщения, он вызывает [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , чтобы получить идентификаторы соответствующих свойств, а затем вызывает [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) для удаления именованных свойств. Также вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения [Каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md) и очищает **INSP\_ONEOFFFLAGS** флаг и **INSP_PROPDEFINITION** флаг, в зависимости от этого свойства таким образом, Outlook 2010 и Outlook 2013 будет выглядеть для именованных свойств, которые были удалены. 
  
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

- [��������� MAPI](mapi-constants.md)

