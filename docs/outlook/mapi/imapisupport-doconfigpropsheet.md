---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429019"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="44145-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="44145-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="44145-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44145-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44145-105">Отображает лист свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44145-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="44145-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="44145-106">Parameters</span></span>

 <span data-ttu-id="44145-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="44145-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="44145-108">[in] Ручка родительского окна листа свойств.</span><span class="sxs-lookup"><span data-stu-id="44145-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="44145-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44145-109">_ulFlags_</span></span>
  
> <span data-ttu-id="44145-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="44145-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="44145-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="44145-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="44145-112">[in] Указатель на название листа свойств.</span><span class="sxs-lookup"><span data-stu-id="44145-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="44145-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="44145-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="44145-114">[in] Указатель на таблицу отображения, описывая элементы управления, которые отображаются на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="44145-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="44145-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="44145-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="44145-116">[in] Указатель на реализацию [IMAPIProp,](imapipropiunknown.md) которая будет использоваться для доступа к свойствам конфигурации, отображаемым на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="44145-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="44145-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="44145-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="44145-118">[in] Нулевой индекс на верхней странице свойства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="44145-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="44145-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44145-119">Return value</span></span>

<span data-ttu-id="44145-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="44145-120">S_OK</span></span> 
  
> <span data-ttu-id="44145-121">Отображается лист свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44145-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44145-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="44145-122">Remarks</span></span>

<span data-ttu-id="44145-123">Для всех объектов поддержки **реализован метод IMAPISupport::D oConfigPropsheet.**</span><span class="sxs-lookup"><span data-stu-id="44145-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="44145-124">**DoConfigPropSheet** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="44145-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="44145-125">Этот стандартный диалоговое окно следует использовать для всех отображаемого свойства конфигурации, чтобы пользователи могли использовать Windows интерфейса.</span><span class="sxs-lookup"><span data-stu-id="44145-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="44145-126">Поставщики услуг звонят **в DoConfigPropSheet** в рамках реализации метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или с кнопки, используемой для отображения сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="44145-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="44145-127">Службы сообщений звонят **в DoConfigPropSheet** из своей функции точки входа в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="44145-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="44145-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="44145-128">Notes to callers</span></span>

<span data-ttu-id="44145-129">Таблицу отображения можно создать с помощью  _параметра lpDisplayTable,_ назвав функцию [BuildDisplayTable](builddisplaytable.md) или с помощью пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="44145-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44145-130">См. также</span><span class="sxs-lookup"><span data-stu-id="44145-130">See also</span></span>



[<span data-ttu-id="44145-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="44145-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="44145-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="44145-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="44145-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="44145-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="44145-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44145-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="44145-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="44145-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="44145-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44145-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="44145-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="44145-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="44145-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="44145-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="44145-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="44145-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

