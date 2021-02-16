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
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="7a3a1-103">Удаление определения настраиваемой формы, сохраненного с сообщением</span><span class="sxs-lookup"><span data-stu-id="7a3a1-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="7a3a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a3a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a3a1-105">В этом разделе показан пример кода на C++, который преобразует сообщение, сохраненное с помощью пользовательского определения формы, в обычное сообщение без определения формы.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="7a3a1-106">В Microsoft Outlook 2010, русская версия Или Microsoft Outlook 2013 можно совместно использовать формы, содержащие настраиваемые страницы форм, публикуя их в библиотеке форм или сохранения соответствующего определения формы в сообщении.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="7a3a1-107">Настраиваемая форма, сохраненная в сообщении, обычно называется "одноавъемной формой", так как она используется только для просмотра конкретного сообщения как разовой формы.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="7a3a1-108">Обычно это происходит, когда форма не публикуется в библиотеке форм, но необходимо, чтобы получатель мог использовать настраиваемую форму при открытии элемента.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="7a3a1-109">Вы можете указать, что форма является односетной в  конструкторе форм, выбрав  определение формы отправки с помощью элемента на странице "Свойства" формы.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="7a3a1-110">Формы, содержащие страницы форм, можно настроить с помощью кода в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7a3a1-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="7a3a1-111">Как правило, размер сообщений, сохраненных с определениями форм, больше.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="7a3a1-112">Из соображений безопасности и хранения Outlook 2010 и Outlook 2013 игнорируют определения форм, сохраненные с любым элементом.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="7a3a1-113">Чтобы преобразовать сообщение, сохраненное с пользовательским определением формы, в одно без него, необходимо удалить четыре именуемые свойства:</span><span class="sxs-lookup"><span data-stu-id="7a3a1-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="7a3a1-114">������������ �������� PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="7a3a1-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="7a3a1-115">������������ �������� PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="7a3a1-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="7a3a1-116">������������ �������� PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="7a3a1-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="7a3a1-117">������������ �������� PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="7a3a1-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="7a3a1-118">Кроме того, необходимо удалить каноническое свойство [PidLidPropertyDefinitionStream,](pidlidpropertydefinitionstream-canonical-property.md) которое содержит определения пользовательских свойств, сохраненных в этом сообщении.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="7a3a1-119">Побочным эффектом удаления этого свойства является то, что объектные модели Outlook 2010 или Outlook 2013 и пользовательский интерфейс Outlook 2010 или Outlook 2013 больше не смогут получить доступ к свойствам пользователей, заданной для сообщения.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="7a3a1-120">Вы по-прежнему можете получить доступ к этим свойствам и их значениям с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="7a3a1-121">Обратите внимание, что если это свойство не удаляется и сообщение сохранено с помощью другого определения формы, каноническое свойство [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) частично перезаписывается новыми данными, а целостность данных не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="7a3a1-122">Если удалить каноническое свойство [PidLidPropertyDefinitionStream,](pidlidpropertydefinitionstream-canonical-property.md)следует также удалить флаг **INSP_PROPDEFINITION** из канонического свойства [PidLidCustomFlag.](pidlidcustomflag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7a3a1-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="7a3a1-123">Следующая функция, принимает в качестве входных параметров указатель на сообщение и индикатор удаления канонического свойства `RemoveOneOff` [PidLidPropertyDefinitionStream.](pidlidpropertydefinitionstream-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7a3a1-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="7a3a1-124">С помощью указателя сообщения он вызывает [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения соответствующих идентификаторов свойств, а затем вызывает [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) для удаления именуемой свойства.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="7a3a1-125">Он также вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения канонического свойства [PidLidCustomFlag](pidlidcustomflag-canonical-property.md) и удаляет флаг **INSP \_ ONEOFFFLAGS** и **флаг INSP_PROPDEFINITION** соответствующим образом из этого свойства, чтобы Outlook 2010 и Outlook 2013 не искать те именовались свойства, которые были удалены.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="7a3a1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7a3a1-126">See also</span></span>

- [<span data-ttu-id="7a3a1-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="7a3a1-127">MAPI Constants</span></span>](mapi-constants.md)

