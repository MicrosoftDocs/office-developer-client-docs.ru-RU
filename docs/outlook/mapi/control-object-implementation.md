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
# <a name="control-object-implementation"></a>Реализация объектов управления

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Объекты управления или объекты, которые поддерживают интерфейс [IMAPIControl : IUnknown,](imapicontroliunknown.md) реализуются поставщиками для добавления функций к кнопке, которая отображается в диалоговом окне MAPI. Объекты управления можно реализовать только для кнопок. 
  
 **IMAPIControl** имеет три метода: [GetLastError,](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)и [Activate](imapicontrol-activate.md). 
  
MAPI вызывает **GetState,** чтобы определить, следует ли отключать кнопку. **GetState** вызван в следующих ситуациях: 
  
- При первом отображке диалоговое окно, в котором отображается кнопка.
    
- Когда для кнопки выдано уведомление о таблице отображения. 
    
Установите для содержимого  _параметра lpulState_ MAPI_DISABLED, если пользователь не может взаимодействовать с кнопкой, MAPI_ENABLED если пользователь может взаимодействовать. 
  
Когда пользователь нажимает кнопку, MAPI вызывает **activate**. **При** активации выполняется задача, связанная с кнопкой. Эта задача может быть в зависимости от поставщика, например отображение диалоговых окна или обновление свойства. Если задача неуспешна, так как пользователь отменил ее, MAPI_E_USER_CANCEL. Для других причин сбоя возвращается соответствующее значение ошибки. 
  
Если задача успешно поставлена и связана с изменением свойства, которое отражается в другом контрольном окне, вызовите [ITableData::HrNotify.](itabledata-hrnotify.md) **HrNotify** вызван для выдачи уведомления таблицы отображения со свойством **PR_CONTROL_ID** свойства [(PidTagControlId)](pidtagcontrolid-canonical-property.md)в TABLE_NOTIFICATION [структуре.](table_notification.md) Не поместите новое значение свойства в структуру; вместо этого возвращаем его при [вызвании IMAPIProp::GetProps.](imapiprop-getprops.md) Хотя обычно уведомление таблицы отображения невозможно использовать для отключения или включения управления, его можно использовать с кнопкой. MAPI обножит измененный контроль, чтобы реагировать на уведомление. 
  
MAPI вызывает метод **GetLastError** этого  MAPI_E_USER_CANCEL. Если **GetLastError** помещает расширенные сведения об ошибке в структуру [MAPIERROR,](mapierror.md) которую он возвращает в содержимом параметра  _lppMAPIError,_ MAPI отображает их для пользователя. 
  
## <a name="see-also"></a>См. также



[Поставщики услуг MAPI](mapi-service-providers.md)

