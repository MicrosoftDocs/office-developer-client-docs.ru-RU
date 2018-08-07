---
title: IMAPIStatusSettingsDialog
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
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809095"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="efc25-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="efc25-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="efc25-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="efc25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="efc25-105">Отображает страницу свойств, который позволяет пользователю изменять конфигурации поставщика услуг, этот метод не поддерживается в состоянии объекты, внедряемые MAPI.</span><span class="sxs-lookup"><span data-stu-id="efc25-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="efc25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efc25-106">Parameters</span></span>

 <span data-ttu-id="efc25-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="efc25-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="efc25-108">[in] Дескриптор родительского окна окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="efc25-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="efc25-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efc25-109">_ulFlags_</span></span>
  
> <span data-ttu-id="efc25-110">[in] Битовая маска флаги, определяющее отображение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="efc25-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="efc25-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="efc25-111">The following flag can be set:</span></span>
    
<span data-ttu-id="efc25-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="efc25-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="efc25-113">Предполагает, что поставщик не следует включать пользователям изменять свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="efc25-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="efc25-114">Этот флаг является всего лишь предложением; его можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="efc25-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efc25-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="efc25-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="efc25-116">S_OK</span></span> 
  
> <span data-ttu-id="efc25-117">Отображается окно свойств конфигурации был успешно.</span><span class="sxs-lookup"><span data-stu-id="efc25-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="efc25-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="efc25-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="efc25-119">Состояние объекта не поддерживает этот метод, как указано в отсутствие флага STATUS_SETTINGS_DIALOG в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="efc25-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efc25-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="efc25-120">Remarks</span></span>

<span data-ttu-id="efc25-121">Метод **IMAPIStatus::SettingsDialog** отображает страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="efc25-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="efc25-122">Все поставщики услуг должен поддерживать метод **SettingsDialog** , но он не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="efc25-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="efc25-123">Поставщиков услуг можно реализовать собственные страницы свойств или реализация, предоставляемая в метод [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="efc25-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="efc25-124">**DoConfigPropsheet** построена на листе свойств чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="efc25-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="efc25-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="efc25-125">Notes to implementers</span></span>

<span data-ttu-id="efc25-126">Если поставщик удаленного транспорта все параметры, необходимо выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="efc25-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="efc25-127">Откройте раздел профиля поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="efc25-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="efc25-128">Получите параметры свойства поставщика транспорта из профиля.</span><span class="sxs-lookup"><span data-stu-id="efc25-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="efc25-129">Отображение в диалоговом окне Параметры свойств.</span><span class="sxs-lookup"><span data-stu-id="efc25-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="efc25-130">Если диалоговое окно позволяет изменять параметры свойств, проверьте, что новые параметры являются допустимыми и хранить их в раздел профиля поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="efc25-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="efc25-131">Возвращает значение S_OK или любой ошибочных значений, возвращаемых во время предыдущего действия.</span><span class="sxs-lookup"><span data-stu-id="efc25-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="efc25-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="efc25-132">Notes to callers</span></span>

<span data-ttu-id="efc25-133">Окно свойств, отображаемое с помощью **SettingsDialog** можно использовать для выполнения различных задач, например следующие:</span><span class="sxs-lookup"><span data-stu-id="efc25-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="efc25-134">Укажите хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efc25-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="efc25-135">Определение порядка транспорта.</span><span class="sxs-lookup"><span data-stu-id="efc25-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="efc25-136">Укажите контейнер по умолчанию адресной книги для просмотра.</span><span class="sxs-lookup"><span data-stu-id="efc25-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="efc25-137">Укажите порядок поиска для разрешения неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="efc25-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="efc25-138">Укажите Личная адресная книга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="efc25-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="efc25-139">Поставщиков услуг можно реализовать страницы свойств, которые доступны для чтения и записи, только для чтения, или набор разрешений, в зависимости от свойства.</span><span class="sxs-lookup"><span data-stu-id="efc25-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="efc25-140">Поставщиков услуг можно реализовать различные разрешения на отдельных свойств с помощью свойства ограничений.</span><span class="sxs-lookup"><span data-stu-id="efc25-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="efc25-141">Режим по умолчанию для свойств — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="efc25-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="efc25-142">Можно запросить таблицы только для чтения свойство, установив флаг UI_READONLY в вызовы **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="efc25-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="efc25-143">Поставщики услуг, которые могут реализовать только для чтения свойств можно сделать.</span><span class="sxs-lookup"><span data-stu-id="efc25-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="efc25-144">Тем не менее так как некоторые поставщики не может переопределить режим по умолчанию, необходимо быть готовым к обработке свойств любого из этих типов.</span><span class="sxs-lookup"><span data-stu-id="efc25-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="efc25-145">Поскольку пользовательский интерфейс всегда участвует в этой операции, только интерактивные клиенты должны вызывать **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="efc25-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="efc25-146">См. также</span><span class="sxs-lookup"><span data-stu-id="efc25-146">See also</span></span>



[<span data-ttu-id="efc25-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="efc25-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="efc25-148">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="efc25-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="efc25-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="efc25-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

