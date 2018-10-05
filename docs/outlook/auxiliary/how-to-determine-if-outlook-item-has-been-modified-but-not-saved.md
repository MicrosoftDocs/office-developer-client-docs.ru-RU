---
title: Определить, если элемент Outlook был изменен, но не сохраняются (Outlook дополнительные справочные материалы по)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65fba557-5fb0-42de-8715-eccda1f3c648
description: This topic shows how to use the dispidFDirty dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.
ms.openlocfilehash: e66a23983a3cc19a7cb51d4b4c3b2c1cee58a793
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395555"
---
# <a name="determine-if-an-outlook-item-has-been-modified-but-not-saved-outlook-auxiliary-reference"></a><span data-ttu-id="568f0-103">Определить, если элемент Outlook был изменен, но не сохраняются (Outlook дополнительные справочные материалы по)</span><span class="sxs-lookup"><span data-stu-id="568f0-103">Determine if an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>

<span data-ttu-id="568f0-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span><span class="sxs-lookup"><span data-stu-id="568f0-104">This topic shows how to use the **dispidFDirty** dispatch ID to invoke the corresponding property on an Outlook item, to see whether the item has been modified and has not been saved.</span></span> 
  
<span data-ttu-id="568f0-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) method to obtain an [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span><span class="sxs-lookup"><span data-stu-id="568f0-105">Given an item object, you can use the [IUnknown::QueryInterface](https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)) method to obtain an [IDispatch](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) interface pointer.</span></span> <span data-ttu-id="568f0-106">Функция в разделе `FIsItemDirty` принимает указатель **IDispatch** _pdisp_, как входного параметра.</span><span class="sxs-lookup"><span data-stu-id="568f0-106">The function in the topic `FIsItemDirty` accepts an **IDispatch** pointer,  _pdisp_, as an input parameter.</span></span>  <span data-ttu-id="568f0-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span><span class="sxs-lookup"><span data-stu-id="568f0-107">`FIsItemDirty` calls the [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) method, specifying **dispidFDirty** as the argument for the  _dispIdMember_ parameter, and the flags  `DISPATCH_METHOD | DISPATCH_PROPERTYGET` for  _wFlags_, to verify whether the item has been modified.</span></span>  <span data-ttu-id="568f0-108">`FIsItemDirty`Возвращает логическое значение (**True** указывает, что элемент имеет несохраненные изменения; в противном случае — **значение False**).</span><span class="sxs-lookup"><span data-stu-id="568f0-108">`FIsItemDirty` returns a Boolean value (**True** to indicate that the item has unsaved changes; otherwise, **False**).</span></span>
  
```cpp
bool FIsItemDirty(IDispatch *pdisp)
{
    DISPPARAMS dispparams;
    UINT uArgErr;
    HRESULT hr = S_OK;
    CComVariant varDirty;
    dispparams.rgvarg = 0;
    dispparams.cArgs = 0;
    dispparams.cNamedArgs = 0;
    dispparams.rgdispidNamedArgs = NULL;
    hr = pdisp->Invoke(dispidFDirty,
        IID_NULL,
        LOCALE_SYSTEM_DEFAULT,
        DISPATCH_METHOD | DISPATCH_PROPERTYGET,
        &amp;dispparams,
        &amp;varDirty,
        NULL,
        &amp;uArgErr);
    return SUCCEEDED(hr) &amp;&amp; varDirty.bVal;
}

```

## <a name="see-also"></a><span data-ttu-id="568f0-109">См. также</span><span class="sxs-lookup"><span data-stu-id="568f0-109">See also</span></span>

- [<span data-ttu-id="568f0-110">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="568f0-110">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)

