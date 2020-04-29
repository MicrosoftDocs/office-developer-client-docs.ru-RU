---
title: Реализация объекта Control
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
# <a name="control-object-implementation"></a><span data-ttu-id="d78e2-103">Реализация объекта Control</span><span class="sxs-lookup"><span data-stu-id="d78e2-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="d78e2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d78e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d78e2-105">Объекты управления или объекты, которые поддерживают интерфейс [имапиконтрол: IUnknown](imapicontroliunknown.md) , реализуются поставщиками для добавления функциональных возможностей кнопки, которая отображается в диалоговом окне MAPI.</span><span class="sxs-lookup"><span data-stu-id="d78e2-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="d78e2-106">Объекты Control могут быть реализованы только для кнопок.</span><span class="sxs-lookup"><span data-stu-id="d78e2-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="d78e2-107">В **имапиконтрол** есть три метода: GetLastError [, и](imapicontrol-getstate.md) [Activate](imapicontrol-activate.md). [GetLastError](imapicontrol-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="d78e2-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="d78e2-108">MAPI вызывает метод/ **State** , чтобы определить, следует ли отключить кнопку.</span><span class="sxs-lookup"><span data-stu-id="d78e2-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="d78e2-109">Метод- **State** вызывается в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="d78e2-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="d78e2-110">При первом отображении диалогового окна, в котором отображается кнопка.</span><span class="sxs-lookup"><span data-stu-id="d78e2-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="d78e2-111">Когда для кнопки выдается уведомление о таблице.</span><span class="sxs-lookup"><span data-stu-id="d78e2-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="d78e2-112">Задайте для параметра _лпулстате_ значение MAPI_DISABLED, если пользователь не может взаимодействовать с кнопкой и MAPI_ENABLED, если пользователь может взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="d78e2-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="d78e2-113">Когда пользователь нажимает кнопку, **активируется**вызов MAPI.</span><span class="sxs-lookup"><span data-stu-id="d78e2-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="d78e2-114">**Активировать** выполняет задачу, связанную с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="d78e2-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="d78e2-115">Эта задача может быть любой, что подходит для вашего поставщика, например отображение диалогового окна или обновление свойства.</span><span class="sxs-lookup"><span data-stu-id="d78e2-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="d78e2-116">Если задача завершается неудачно, так как пользователь отменил действие, возвращается MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="d78e2-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="d78e2-117">Для других причин сбоя возвращает соответствующее значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="d78e2-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="d78e2-118">Если задача выполнена успешно и связана с изменением свойства, которое отражается в другом элементе управления в диалоговом окне, вызовите метод [итабледата:: хрнотифи](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="d78e2-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="d78e2-119">**Хрнотифи** вызывается для выпуска уведомления таблицы отображения со свойством Changed свойства **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) в структуре [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d78e2-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="d78e2-120">Не помещайте новое значение свойства в структуру; Вместо этого возвращается этот метод, когда вызывается метод [IMAPIProp::-PROPS](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d78e2-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="d78e2-121">Хотя обычно уведомления в таблице отображения нельзя использовать для отключения или включения элемента управления, его можно использовать с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="d78e2-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="d78e2-122">MAPI обновит измененный элемент управления, чтобы он отвечал на уведомление.</span><span class="sxs-lookup"><span data-stu-id="d78e2-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="d78e2-123">MAPI вызывает метод **GetLastError** элемента управления, если функция **Activate** возвращает ошибку, отличную от MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="d78e2-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="d78e2-124">Если **GetLastError** размещает расширенные сведения об ошибке в структуре [мапиеррор](mapierror.md) , возвращаемой в содержимом параметра _лппмапиеррор_ , MAPI отображает его для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d78e2-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d78e2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d78e2-125">See also</span></span>



[<span data-ttu-id="d78e2-126">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="d78e2-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

