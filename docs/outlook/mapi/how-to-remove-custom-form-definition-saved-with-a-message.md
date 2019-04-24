---
title: Удаление определения настраиваемой формы, сохраненного с сообщением
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345936"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="3e75a-103">Удаление определения настраиваемой формы, сохраненного с сообщением</span><span class="sxs-lookup"><span data-stu-id="3e75a-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="3e75a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e75a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e75a-105">В этом разделе показан пример кода на языке C++, который преобразует сообщение, сохраненное с настраиваемым определением формы, в обычное сообщение без определения формы.</span><span class="sxs-lookup"><span data-stu-id="3e75a-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="3e75a-106">В Microsoft Outlook 2010 или Microsoft Outlook 2013 можно совместно использовать формы, содержащие настраиваемые страницы форм, либо опубликовав их в библиотеке форм, либо сохраняя соответствующее определение формы с сообщением.</span><span class="sxs-lookup"><span data-stu-id="3e75a-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="3e75a-107">Настраиваемая форма, сохраненная с сообщением, обычно называется "одноразовой формой", так как эта форма доступна только для просмотра определенного сообщения в качестве одноразового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3e75a-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="3e75a-108">Это обычно делается, когда форма не публикуется в библиотеке форм, но вы хотите, чтобы получатель использовал настраиваемую форму при открытии элемента.</span><span class="sxs-lookup"><span data-stu-id="3e75a-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="3e75a-109">Вы можете указать форму в качестве одноразовой в конструкторе форм, установив флажок **Отправить определение формы с элементом** на странице **свойств** формы.</span><span class="sxs-lookup"><span data-stu-id="3e75a-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="3e75a-110">Формы, содержащие страницы форм, можно изменять с помощью кода в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="3e75a-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="3e75a-111">Сообщения, сохраненные с определениями форм, обычно имеют больший размер.</span><span class="sxs-lookup"><span data-stu-id="3e75a-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="3e75a-112">В целях обеспечения безопасности и хранения Outlook 2010 и Outlook 2013 игнорируют определения форм, сохраненные с любым элементом.</span><span class="sxs-lookup"><span data-stu-id="3e75a-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="3e75a-113">Чтобы преобразовать сообщение, сохраненное с настраиваемым определением формы, на одно без, необходимо удалить четыре именованных свойства:</span><span class="sxs-lookup"><span data-stu-id="3e75a-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="3e75a-114">������������ �������� PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="3e75a-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="3e75a-115">������������ �������� PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="3e75a-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="3e75a-116">������������ �������� PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="3e75a-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="3e75a-117">������������ �������� PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="3e75a-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="3e75a-118">Кроме того, следует удалить [канонИческое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) , которое содержит определения настраиваемых свойств, сохраненных с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="3e75a-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="3e75a-119">Побочным результатом удаления этого свойства является то, что объектные модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получать доступ к свойствам пользователей, которые были заданы для сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e75a-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="3e75a-120">Вы по-прежнему можете получать доступ к этим свойствам и их значениям с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e75a-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="3e75a-121">Обратите внимание, что если не удалить это свойство, а сообщение сохранено с другим определением формы, [канонИческое свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично перезаписывается новыми данными, а целостность данных не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3e75a-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="3e75a-122">Если удалить каноническое [свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), необходимо также удалить флаг **инсп_пропдефинитион** из [каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="3e75a-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="3e75a-123">Приведенная ниже функция `RemoveOneOff`принимает указатель на сообщение в качестве входных параметров и определяет, следует ли удалить каноническое [свойство PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="3e75a-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="3e75a-124">С помощью указателя сообщения вызывается метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить соответствующие идентификаторы свойств, а затем вызывает [IMAPIProp::D елетепропс](imapiprop-deleteprops.md) для удаления именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="3e75a-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="3e75a-125">Кроме того, он вызывает [IMAPIProp:: PROPS](imapiprop-getprops.md) , чтобы [получить каноническое свойство PidLidCustomFlag](pidlidcustomflag-canonical-property.md) , и очищает флаг **инсп\_онеофффлагс** и **инсп_пропдефинитион** , в соответствии с этим свойством, чтобы Outlook 2010 и Outlook 2013 не будет искать удаленные именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3e75a-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="3e75a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3e75a-126">See also</span></span>

- [<span data-ttu-id="3e75a-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="3e75a-127">MAPI Constants</span></span>](mapi-constants.md)

