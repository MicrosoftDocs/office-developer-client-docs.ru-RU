---
title: Удалите Определение настраиваемой формы, сохраненных в сообщение
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 4b12824542a1408a364452eb6587122ec66412d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594455"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="b8d7a-103">Удалите Определение настраиваемой формы, сохраненных в сообщение</span><span class="sxs-lookup"><span data-stu-id="b8d7a-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="b8d7a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8d7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8d7a-105">В этом разделе приводится пример кода c++, который преобразует сообщения, который был сохранен с определениями настраиваемых форм для регулярного сообщение без определения формы.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="b8d7a-106">В Microsoft Outlook 2010 или Microsoft Outlook 2013 совместное использование форм, содержащих настраиваемые страницы форм по их публикации в библиотеке форм или сохранения соответствующее определение формы с сообщением.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="b8d7a-107">Настраиваемая форма, сохраненных в сообщение режимами «одноразовых формы,» с момента формы совместно используется только для просмотра отдельного сообщения как одноразовых экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="b8d7a-108">Обычно это делается при формы не публикуется в библиотеке форм, но разрешить получателю использовать настраиваемую форму при открытии элемента.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="b8d7a-109">Можно указать, что формы — одного раза в конструкторе форм, установив флажок **Отправлять вместе с элементом** на странице **свойств** формы.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="b8d7a-110">Форм, содержащих страниц форм можно настроить с помощью кода в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="b8d7a-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="b8d7a-111">Сообщения, которые будут сохранены с определения формы, обычно больше по размеру.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="b8d7a-112">Для безопасности и для обеспечения хранения Outlook 2010 и Outlook 2013 игнорировать определения форм, сохраненных в любой элемент.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="b8d7a-113">Чтобы преобразовать сообщение, в котором сохраняется с определениями настраиваемых форм к одному без, необходимо удалить четыре именованных свойств:</span><span class="sxs-lookup"><span data-stu-id="b8d7a-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="b8d7a-114">������������ �������� PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="b8d7a-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="b8d7a-115">������������ �������� PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="b8d7a-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="b8d7a-116">������������ �������� PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="b8d7a-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="b8d7a-117">������������ �������� PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="b8d7a-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="b8d7a-118">Кроме того следует удалить [PidLidPropertyDefinitionStream каноническое свойство](pidlidpropertydefinitionstream-canonical-property.md) , которое содержит определения пользовательских свойств, сохраненных в этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="b8d7a-119">Влияние со стороны удаления это свойство является то, что объектной модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получать доступ к свойствам пользователя, которые были установлены в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="b8d7a-120">По-прежнему можно получить доступ к эти свойства и их значения через MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="b8d7a-121">Обратите внимание, что если это свойство не удаляйте и сообщение сохраняется с другой определение формы, [Свойство каноническое PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично заменены новыми данными и целостность данных не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="b8d7a-122">При удалении [Каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)также удалите флаг **INSP_PROPDEFINITION** из [PidLidCustomFlag каноническое свойство](pidlidcustomflag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="b8d7a-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="b8d7a-123">Следующая функция `RemoveOneOff`, принимает в качестве входных параметров указатель на сообщение и индикатор необходимость удаления [Каноническое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="b8d7a-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="b8d7a-124">С помощью указателя мыши сообщения, он вызывает [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , чтобы получить идентификаторы соответствующих свойств, а затем вызывает [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) для удаления именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="b8d7a-125">Также вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения [Каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md) и очищает **INSP\_ONEOFFFLAGS** флаг и **INSP_PROPDEFINITION** флаг, в зависимости от этого свойства таким образом, Outlook 2010 и Outlook 2013 будет выглядеть для именованных свойств, которые были удалены.</span><span class="sxs-lookup"><span data-stu-id="b8d7a-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b8d7a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b8d7a-126">See also</span></span>

- [<span data-ttu-id="b8d7a-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="b8d7a-127">MAPI Constants</span></span>](mapi-constants.md)

