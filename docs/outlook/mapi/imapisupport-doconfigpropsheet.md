---
title: имаписуппортдоконфигпропшит
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
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="d31b3-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="d31b3-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="d31b3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d31b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d31b3-105">Отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d31b3-105">Displays a configuration property sheet.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d31b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d31b3-106">Parameters</span></span>

 <span data-ttu-id="d31b3-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="d31b3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d31b3-108">возврата Дескриптор родительского окна страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="d31b3-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="d31b3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d31b3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d31b3-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d31b3-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d31b3-111">_лпсзтитле_</span><span class="sxs-lookup"><span data-stu-id="d31b3-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="d31b3-112">возврата Указатель на название страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="d31b3-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="d31b3-113">_лпдисплайтабле_</span><span class="sxs-lookup"><span data-stu-id="d31b3-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="d31b3-114">возврата Указатель на таблицу отображения, описывающую элементы управления, которые отображаются на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="d31b3-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="d31b3-115">_лпконфигдата_</span><span class="sxs-lookup"><span data-stu-id="d31b3-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="d31b3-116">возврата Указатель на реализацию [IMAPIProp](imapipropiunknown.md) , который будет использоваться для доступа к свойствам конфигурации, которые будут отображаться на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="d31b3-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="d31b3-117">_ултоппаже_</span><span class="sxs-lookup"><span data-stu-id="d31b3-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="d31b3-118">возврата Индекс с отсчетом от нуля до верхней страницы листа свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d31b3-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d31b3-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d31b3-119">Return value</span></span>

<span data-ttu-id="d31b3-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d31b3-120">S_OK</span></span> 
  
> <span data-ttu-id="d31b3-121">Отображается страница свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d31b3-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d31b3-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="d31b3-122">Remarks</span></span>

<span data-ttu-id="d31b3-123">Метод **имаписуппорт::D оконфигпропшит** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="d31b3-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="d31b3-124">**Доконфигпропшит** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="d31b3-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="d31b3-125">Это стандартное диалоговое окно следует использовать для всех свойств конфигурации, чтобы пользователи могли воспользоваться единообразным интерфейсом Windows.</span><span class="sxs-lookup"><span data-stu-id="d31b3-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="d31b3-126">Поставщики услуг вызывают **доконфигпропшит** в рамках реализации метода [Имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) или из кнопки, используемой для отображения сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="d31b3-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="d31b3-127">Службы сообщений вызывают **доконфигпропшит** из функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d31b3-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d31b3-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d31b3-128">Notes to callers</span></span>

<span data-ttu-id="d31b3-129">Вы можете создать отображаемую таблицу, на которую указывает параметр _лпдисплайтабле_ , вызвав функцию [буилддисплайтабле](builddisplaytable.md) или пользовательский код.</span><span class="sxs-lookup"><span data-stu-id="d31b3-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d31b3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d31b3-130">See also</span></span>



[<span data-ttu-id="d31b3-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d31b3-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="d31b3-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="d31b3-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="d31b3-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d31b3-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d31b3-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d31b3-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d31b3-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="d31b3-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="d31b3-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d31b3-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="d31b3-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d31b3-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="d31b3-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="d31b3-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="d31b3-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d31b3-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

