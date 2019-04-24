---
title: Имапистатуссеттингсдиалог
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331544"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="3ea1b-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="3ea1b-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="3ea1b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ea1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ea1b-105">Отображает страницу свойств, с помощью которой пользователь может изменить конфигурацию поставщика услуг этот метод не поддерживается в объектах состояния, реализованных MAPI.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3ea1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ea1b-106">Parameters</span></span>

 <span data-ttu-id="3ea1b-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="3ea1b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3ea1b-108">возврата Дескриптор родительского окна на странице свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="3ea1b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ea1b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3ea1b-110">возврата Битовая маска флагов, которые управляют отображением страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="3ea1b-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3ea1b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3ea1b-112">УИ_РЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="3ea1b-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="3ea1b-113">Предполагает, что поставщик не должен предоставлять пользователям возможность изменять свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="3ea1b-114">Этот флаг является только предложением; его можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ea1b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ea1b-115">Return value</span></span>

<span data-ttu-id="3ea1b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ea1b-116">S_OK</span></span> 
  
> <span data-ttu-id="3ea1b-117">Страница свойств конфигурации успешно отображена.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="3ea1b-118">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="3ea1b-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3ea1b-119">Объект Status не поддерживает этот метод, как указано в отсутствие флага СТАТУС_СЕТТИНГС_ДИАЛОГ в свойстве **пр_ресаурце_месодс** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3ea1b-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ea1b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ea1b-120">Remarks</span></span>

<span data-ttu-id="3ea1b-121">Метод **имапистатус:: сеттингсдиалог** отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="3ea1b-122">Все поставщики служб должны поддерживать метод **сеттингсдиалог** , но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="3ea1b-123">Поставщики услуг могут реализовывать собственные страницы свойств или использовать реализацию, предоставленную в методе [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea1b-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="3ea1b-124">**Доконфигпропшит** создает страницу свойств для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ea1b-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3ea1b-125">Notes to implementers</span></span>

<span data-ttu-id="3ea1b-126">Если у удаленного поставщика транспорта есть параметры, он должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3ea1b-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="3ea1b-127">Откройте раздел Профиль поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="3ea1b-128">Получите параметры свойства поставщика транспорта из профиля.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="3ea1b-129">Отображение параметров свойства в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="3ea1b-130">Если диалоговое окно позволяет редактировать параметры свойства, убедитесь, что новые параметры являются допустимыми, и сохраните их обратно в разделе профиля поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="3ea1b-131">Возвращает значение S_OK или любые ошибки, возвращенные в ходе выполнения предыдущих действий.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="3ea1b-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3ea1b-132">Notes to callers</span></span>

<span data-ttu-id="3ea1b-133">С помощью страницы свойств, отображаемой в **сеттингсдиалог** , можно выполнять различные задачи, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="3ea1b-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="3ea1b-134">Укажите хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="3ea1b-135">Указание транспортного заказа.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="3ea1b-136">Укажите контейнер адресной книги по умолчанию для просмотра.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="3ea1b-137">Указание порядка поиска для разрешения неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="3ea1b-138">Укажите личную адресную книгу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="3ea1b-139">Поставщики услуг могут реализовывать страницы свойств, доступные для чтения и записи, только для чтения или для разных разрешений, в зависимости от свойства.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="3ea1b-140">Поставщики услуг могут реализовать различные разрешения для отдельных свойств, задав ограничения свойств.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="3ea1b-141">Режим по умолчанию для страниц свойств доступен для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="3ea1b-142">Можно запросить таблицы свойств, доступные только для чтения, установив флаг УИ_РЕАДОНЛИ в вызовах **сеттингсдиалог**.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="3ea1b-143">Это можно сделать с поставщиками услуг, которые могут реализовать вкладки свойств, доступные только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="3ea1b-144">Тем не менее, так как некоторые поставщики услуг не могут переопределить режим по умолчанию, необходимо подготовиться к обработке страниц свойств любого типа.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="3ea1b-145">Так как пользовательский интерфейс всегда участвует в этой операции, только Интерактивные клиенты должны вызывать **сеттингсдиалог**.</span><span class="sxs-lookup"><span data-stu-id="3ea1b-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ea1b-146">См. также</span><span class="sxs-lookup"><span data-stu-id="3ea1b-146">See also</span></span>



[<span data-ttu-id="3ea1b-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="3ea1b-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="3ea1b-148">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="3ea1b-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="3ea1b-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3ea1b-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

