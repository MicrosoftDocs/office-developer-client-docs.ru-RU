---
title: Реализация объекта элемента управления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565832"
---
# <a name="control-object-implementation"></a><span data-ttu-id="ed987-103">Реализация объекта элемента управления</span><span class="sxs-lookup"><span data-stu-id="ed987-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="ed987-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed987-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed987-105">Управлять объектов или объектов, которые поддерживают [IMAPIControl: IUnknown](imapicontroliunknown.md) интерфейс, реализуемые поставщиками, чтобы добавить функциональные возможности для кнопки, которое отображается в диалоговом окне MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed987-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="ed987-106">Объекты элементов управления можно реализовать только для кнопок.</span><span class="sxs-lookup"><span data-stu-id="ed987-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="ed987-107">**IMAPIControl** имеет три метода: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)и [активировать](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="ed987-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="ed987-108">MAPI вызывает **GetState** , чтобы определить, следует ли отключить кнопку.</span><span class="sxs-lookup"><span data-stu-id="ed987-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="ed987-109">**GetState** вызывается в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="ed987-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="ed987-110">При первом отображении диалоговое окно, на котором отображается кнопка.</span><span class="sxs-lookup"><span data-stu-id="ed987-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="ed987-111">Для кнопки выпуска отображать уведомления в таблице.</span><span class="sxs-lookup"><span data-stu-id="ed987-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="ed987-112">Значение содержимого параметра _lpulState_ MAPI_DISABLED, если пользователь не может взаимодействовать с кнопки и MAPI_ENABLED, если пользователь.</span><span class="sxs-lookup"><span data-stu-id="ed987-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="ed987-113">При нажатии пользователем кнопки MAPI вызывает **активировать**.</span><span class="sxs-lookup"><span data-stu-id="ed987-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="ed987-114">**Активировать** выполняет задачу, которая была связана с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="ed987-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="ed987-115">Эта задача может быть любым подходящую для поставщика, например, отображение диалогового окна или обновлении свойства.</span><span class="sxs-lookup"><span data-stu-id="ed987-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="ed987-116">Если задача завершается неудачно, так как пользователь отменил ее, возвратите MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="ed987-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="ed987-117">Для других причины сбоя возврата соответствующего значения ошибки.</span><span class="sxs-lookup"><span data-stu-id="ed987-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="ed987-118">Если задача выполнена успешно и связан с изменения свойства, которое отображается в другой элемент управления в диалоговом окне, вызовите [ITableData::HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="ed987-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="ed987-119">Для выдачи уведомление таблицы со свойством **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) измененное свойство в структуре [TABLE_NOTIFICATION](table_notification.md) называется **HrNotify** .</span><span class="sxs-lookup"><span data-stu-id="ed987-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="ed987-120">Не размещайте новое значение свойства в структуре; Вместо этого возвращается при вызове [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ed987-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="ed987-121">Несмотря на то, что обычно отображать уведомления в таблице не может использоваться для отключения и включения элемента управления, его можно использовать с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="ed987-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="ed987-122">MAPI будет обновлять измененный элемент управления в ответ на уведомление.</span><span class="sxs-lookup"><span data-stu-id="ed987-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="ed987-123">MAPI вызывает метод **GetLastError** элемента управления, когда **активировать** возвращает ошибку, отличный от MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="ed987-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="ed987-124">**GetLastError** помещает расширенные сведения об ошибке в структуре [MAPIERROR](mapierror.md) , которое возвращает содержимое параметр _lppMAPIError_ , MAPI отображает для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed987-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed987-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ed987-125">See also</span></span>



[<span data-ttu-id="ed987-126">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="ed987-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

