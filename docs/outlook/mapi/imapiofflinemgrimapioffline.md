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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270093"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поддерживает регистрацию для вызовов уведомлений об изменениях состояния подключения учетной записи пользователя.
  
|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |msmapi32.dll  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[Консультация](imapiofflinemgr-advise.md) <br/> |Регистрирует для уведомлений об изменениях подключения.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Удаляет заданную регистрацию для вызовов уведомлений.  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
| *Член-заметель*  <br/> | *Этот член является местоимящиком и не поддерживается.*  <br/> |
   
## <a name="remarks"></a>Примечания

При открытии автономного объекта для профиля учетной записи пользователя с помощью **[HrOpenOfflineObj](hropenofflineobj.md)** клиент получает автономный объект, который поддерживает **IMAPIOfflineMgr.** 
  
Так как этот интерфейс наследуется от **[IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** клиент может запросить этот интерфейс (с помощью **[IUnknown::QueryInterface),](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** чтобы получить объект, который поддерживает **[IMAPIOffline](imapiofflineiunknown.md)**. Затем клиент может узнать о возможностях автоответа автономного объекта (путем вызова **[IMAPIOffline::GetCapabilities)](imapioffline-getcapabilities.md)** и настроить функцию вызова (с помощью **IMAPIOfflineMgr::Advise).** 
  
Большинство членов этого интерфейса являются замесятелями, зарезервированными для внутреннего использования Outlook, и могут изменяться. Вызыватели этого интерфейса должны использовать не-замедерые члены, только как описано в документации.
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

