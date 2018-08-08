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
ms.openlocfilehash: 644fad96c8aec3701233351469a84ef93341b397
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809022"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Относится к**: Outlook 
  
Поддерживает регистрации для обратных вызовов уведомление об изменениях состояния подключения к учетной записи пользователя.
  
|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
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
   
## <a name="remarks"></a>Замечания

При открытии автономного объекта для профиля учетной записи пользователя, с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**. 
  
Так как этот интерфейс наследует от **[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)**, клиент может запросить этот интерфейс (с помощью **[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)** ) для получения объекта, который поддерживает **[IMAPIOffline](imapiofflineiunknown.md)**. Клиент можно узнать о возможностях обратного вызова автономного объекта (по вызову **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) и нажмите кнопку Настройка обратных вызовов (с помощью **IMAPIOfflineMgr::Advise** ). 
  
Большая часть члены этого интерфейса являются заполнители зарезервировано для внутреннего использования Outlook и могут быть изменены. Вызывающие этот интерфейс необходимо использовать члены являющиеся заполнителями только в документации.
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

