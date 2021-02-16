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
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439732"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="99862-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="99862-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="99862-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99862-105">Отображает лист свойств, позволяющий пользователю изменить конфигурацию поставщика услуг. Этот метод не поддерживается в объектах состояния, реализуемых MAPI.</span><span class="sxs-lookup"><span data-stu-id="99862-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="99862-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99862-106">Parameters</span></span>

 <span data-ttu-id="99862-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="99862-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="99862-108">[in] Окне родительского окна таблицы свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99862-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="99862-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99862-109">_ulFlags_</span></span>
  
> <span data-ttu-id="99862-110">[in] Битоваяmas флагов, которая управляет отображением листа свойств.</span><span class="sxs-lookup"><span data-stu-id="99862-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="99862-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="99862-111">The following flag can be set:</span></span>
    
<span data-ttu-id="99862-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="99862-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="99862-113">Предполагается, что поставщик не должен позволить пользователям изменять свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99862-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="99862-114">Этот флаг является лишь предложением; его можно проигнорировать.</span><span class="sxs-lookup"><span data-stu-id="99862-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99862-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99862-115">Return value</span></span>

<span data-ttu-id="99862-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="99862-116">S_OK</span></span> 
  
> <span data-ttu-id="99862-117">Таблица свойств конфигурации успешно отобразилась.</span><span class="sxs-lookup"><span data-stu-id="99862-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="99862-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="99862-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="99862-119">Объект состояния не поддерживает этот метод, на что указывает отсутствие флага STATUS_SETTINGS_DIALOG в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="99862-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99862-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="99862-120">Remarks</span></span>

<span data-ttu-id="99862-121">Метод **IMAPIStatus::SettingsDialog** отображает таблицу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99862-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="99862-122">Все поставщики услуг должны поддерживать метод **SettingsDialog,** но он не требуется.</span><span class="sxs-lookup"><span data-stu-id="99862-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="99862-123">Поставщики служб могут реализовать собственные листы свойств или использовать реализацию, предоставленную в [методе IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="99862-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="99862-124">**DoConfigPropsheet** создает лист свойств чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="99862-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99862-125">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="99862-125">Notes to implementers</span></span>

<span data-ttu-id="99862-126">Если у удаленного поставщика транспорта есть какие-либо параметры, он должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="99862-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="99862-127">Откройте раздел профиля поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="99862-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="99862-128">Получите параметры свойств поставщика транспорта из профиля.</span><span class="sxs-lookup"><span data-stu-id="99862-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="99862-129">Отображение параметров свойств в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="99862-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="99862-130">Если диалоговое окно позволяет редактировать параметры свойств, убедитесь, что новые параметры действительны, и храните их обратно в разделе профиля поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="99862-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="99862-131">Возвращает S_OK или любые значения ошибок, возвращенные на предыдущих шагах.</span><span class="sxs-lookup"><span data-stu-id="99862-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="99862-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="99862-132">Notes to callers</span></span>

<span data-ttu-id="99862-133">Лист свойств, отображаемой в **SettingsDialog,** можно использовать для выполнения различных задач, например:</span><span class="sxs-lookup"><span data-stu-id="99862-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="99862-134">Укажите хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="99862-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="99862-135">Укажите порядок транспорта.</span><span class="sxs-lookup"><span data-stu-id="99862-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="99862-136">Укажите контейнер адресной книги по умолчанию для просмотра.</span><span class="sxs-lookup"><span data-stu-id="99862-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="99862-137">Укажите порядок поиска для разрешения неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="99862-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="99862-138">Укажите личную адресную книгу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="99862-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="99862-139">Поставщики служб могут реализовать листы свойств, которые являются чтением и написанием, только для чтения или сочетанием разрешений, в зависимости от свойства.</span><span class="sxs-lookup"><span data-stu-id="99862-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="99862-140">Поставщики услуг могут реализовать различные разрешения для отдельных свойств, установив ограничения свойств.</span><span class="sxs-lookup"><span data-stu-id="99862-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="99862-141">Режим по умолчанию для листов свойств — чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="99862-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="99862-142">Можно запросить листы свойств только для чтения, установив флаг UI_READONLY в вызовах **SettingsDialog.**</span><span class="sxs-lookup"><span data-stu-id="99862-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="99862-143">Это могут сделать поставщики услуг, способные реализовать листы свойств только для чтения.</span><span class="sxs-lookup"><span data-stu-id="99862-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="99862-144">Однако, поскольку некоторые поставщики услуг не могут переопределять режим по умолчанию, необходимо быть готовым обрабатывать листы свойств любого типа.</span><span class="sxs-lookup"><span data-stu-id="99862-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="99862-145">Так как в этой операции всегда участвует пользовательский интерфейс, только интерактивные клиенты должны **вызывать SettingsDialog.**</span><span class="sxs-lookup"><span data-stu-id="99862-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99862-146">См. также</span><span class="sxs-lookup"><span data-stu-id="99862-146">See also</span></span>



[<span data-ttu-id="99862-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="99862-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="99862-148">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="99862-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="99862-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="99862-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

