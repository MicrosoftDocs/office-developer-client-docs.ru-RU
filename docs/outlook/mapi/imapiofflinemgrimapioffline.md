---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397053"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживает регистрации для обратных вызовов уведомление об изменениях состояния подключения к учетной записи пользователя.
  
|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Уведомить](imapiofflinemgr-advise.md) <br/> |Регистрация для обратных вызовов уведомлений об изменении подключения.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Удаляет указанного регистрацию для обратных вызовов уведомлений.  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
| *Заполнитель члена*  <br/> | *Этот член — это и не поддерживается.*  <br/> |
   
## <a name="remarks"></a>Примечания

При открытии автономного объекта для профиля учетной записи пользователя, с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**. 
  
Так как этот интерфейс наследует от **[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)**, клиент может запросить этот интерфейс (с помощью **[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) для получения объекта, который поддерживает **[IMAPIOffline](imapiofflineiunknown.md)**. Клиент можно узнать о возможностях обратного вызова автономного объекта (по вызову **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) и нажмите кнопку Настройка обратных вызовов (с помощью **IMAPIOfflineMgr::Advise** ). 
  
Большая часть члены этого интерфейса являются заполнители зарезервировано для внутреннего использования Outlook и могут быть изменены. Вызывающие этот интерфейс необходимо использовать члены являющиеся заполнителями только в документации.
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[Константы MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

