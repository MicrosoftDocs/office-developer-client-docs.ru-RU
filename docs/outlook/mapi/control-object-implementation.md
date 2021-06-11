---
title: Управление реализацией объектов
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
# <a name="control-object-implementation"></a>Управление реализацией объектов

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Объекты управления или объекты, поддерживаюшие [интерфейс IMAPIControl : IUnknown,](imapicontroliunknown.md) реализуются поставщиками для добавления функций в кнопку, которая отображается в диалоговом окне MAPI. Объекты управления можно реализовать только для кнопок. 
  
 **IMAPIControl** имеет три метода: [GetLastError,](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)и [Activate.](imapicontrol-activate.md) 
  
MAPI вызывает **GetState,** чтобы определить, следует ли отключить кнопку. **GetState** называется в следующих ситуациях: 
  
- Когда диалоговое окно, на котором появится кнопка, сначала отображается.
    
- При выдаче уведомления о таблице отображения для кнопки. 
    
Установите содержимое параметра  _lpulState_ MAPI_DISABLED, если пользователь не может взаимодействовать с кнопкой и MAPI_ENABLED, если пользователь может взаимодействовать. 
  
Когда пользователь нажимает кнопку, вызовы MAPI **активируются.** **Активация** выполняет задачу, связанную с кнопкой. Эта задача может быть уместна для поставщика, например отобразить диалоговое окно или обновить свойство. Если задача неуспешна из-за отмены пользователем ее, MAPI_E_USER_CANCEL. Для других причин сбоя возвращаем соответствующее значение ошибки. 
  
Если задача является успешной и связана с изменением свойства, которое отражено в другом окне управления в диалоговом окне, позвоните [в ITableData::HrNotify](itabledata-hrnotify.md). **HrNotify** вызван для выпуска уведомления таблицы отображения с свойством PR_CONTROL_ID **свойства** [(PidTagControlId)](pidtagcontrolid-canonical-property.md)в [структуре](table_notification.md) TABLE_NOTIFICATION. Не поместите новое значение свойства в структуру; вместо этого верни его, когда [называется IMAPIProp::GetProps.](imapiprop-getprops.md) Хотя обычно для отключения или включения управления нельзя использовать уведомление таблицы отображения, его можно использовать с помощью кнопки. MAPI обновит измененный контроль, чтобы ответить на уведомление. 
  
MAPI вызывает метод **GetLastError** управления, когда **активация** возвращает ошибку, не MAPI_E_USER_CANCEL. Если **GetLastError** помещает расширенные сведения об ошибках в структуре [MAPIERROR,](mapierror.md) возвращаемой в содержимом параметра  _lppMAPIError,_ MAPI отображает ее для пользователя. 
  
## <a name="see-also"></a>См. также



[Поставщики услуг MAPI](mapi-service-providers.md)

