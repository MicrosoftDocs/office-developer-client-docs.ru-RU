---
title: Реализация объектов управления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422609"
---
# <a name="control-object-implementation"></a><span data-ttu-id="b36b8-103">Реализация объектов управления</span><span class="sxs-lookup"><span data-stu-id="b36b8-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="b36b8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b36b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b36b8-105">Объекты управления или объекты, которые поддерживают интерфейс [IMAPIControl : IUnknown,](imapicontroliunknown.md) реализуются поставщиками для добавления функций к кнопке, которая отображается в диалоговом окне MAPI.</span><span class="sxs-lookup"><span data-stu-id="b36b8-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="b36b8-106">Объекты управления можно реализовать только для кнопок.</span><span class="sxs-lookup"><span data-stu-id="b36b8-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="b36b8-107">**IMAPIControl** имеет три метода: [GetLastError,](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)и [Activate](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="b36b8-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="b36b8-108">MAPI вызывает **GetState,** чтобы определить, следует ли отключать кнопку.</span><span class="sxs-lookup"><span data-stu-id="b36b8-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="b36b8-109">**GetState** вызван в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="b36b8-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="b36b8-110">При первом отображке диалоговое окно, в котором отображается кнопка.</span><span class="sxs-lookup"><span data-stu-id="b36b8-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="b36b8-111">Когда для кнопки выдано уведомление о таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="b36b8-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="b36b8-112">Установите для содержимого  _параметра lpulState_ MAPI_DISABLED, если пользователь не может взаимодействовать с кнопкой, MAPI_ENABLED если пользователь может взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="b36b8-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="b36b8-113">Когда пользователь нажимает кнопку, MAPI вызывает **activate**.</span><span class="sxs-lookup"><span data-stu-id="b36b8-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="b36b8-114">**При** активации выполняется задача, связанная с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="b36b8-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="b36b8-115">Эта задача может быть в зависимости от поставщика, например отображение диалоговых окна или обновление свойства.</span><span class="sxs-lookup"><span data-stu-id="b36b8-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="b36b8-116">Если задача неуспешна, так как пользователь отменил ее, MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="b36b8-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="b36b8-117">Для других причин сбоя возвращается соответствующее значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b36b8-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="b36b8-118">Если задача успешно поставлена и связана с изменением свойства, которое отражается в другом контрольном окне, вызовите [ITableData::HrNotify.](itabledata-hrnotify.md)</span><span class="sxs-lookup"><span data-stu-id="b36b8-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="b36b8-119">**HrNotify** вызван для выдачи уведомления таблицы отображения со свойством **PR_CONTROL_ID** свойства [(PidTagControlId)](pidtagcontrolid-canonical-property.md)в TABLE_NOTIFICATION [структуре.](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="b36b8-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="b36b8-120">Не поместите новое значение свойства в структуру; вместо этого возвращаем его при [вызвании IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="b36b8-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="b36b8-121">Хотя обычно уведомление таблицы отображения невозможно использовать для отключения или включения управления, его можно использовать с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="b36b8-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="b36b8-122">MAPI обножит измененный контроль, чтобы реагировать на уведомление.</span><span class="sxs-lookup"><span data-stu-id="b36b8-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="b36b8-123">MAPI вызывает метод **GetLastError** этого  MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="b36b8-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="b36b8-124">Если **GetLastError** помещает расширенные сведения об ошибке в структуру [MAPIERROR,](mapierror.md) которую он возвращает в содержимом параметра  _lppMAPIError,_ MAPI отображает их для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b36b8-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b36b8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b36b8-125">See also</span></span>



[<span data-ttu-id="b36b8-126">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="b36b8-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

