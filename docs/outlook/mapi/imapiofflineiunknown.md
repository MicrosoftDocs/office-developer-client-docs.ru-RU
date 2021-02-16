---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321268"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения для автономного объекта.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Запрос к [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Задает текущее состояние автономного объекта в сетевом или автономном режиме.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Получает условия, для которых автономный объект поддерживает вызовы.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Получает текущее сетевое или автономное состояние автономного объекта.  <br/> |
| *Член-заметель*  <br/> |Этот член является местоимящиком и не поддерживается.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получения автономного объекта, который поддерживает **IMAPIOfflineMgr.** Так как **IMAPIOfflineMgr** наследуется от [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)клиент может запросить этот интерфейс (с помощью [IUnknown::QueryInterface),](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)чтобы получить указатель на указатель интерфейса **для IMAPIOffline** для автономного объекта. Затем клиент может получить или установить текущее состояние объекта или узнать о возможностях вызова объекта (путем вызова **IMAPIOffline::GetCapabilities)** и настроить функцию перезаписи вызовов с помощью **[IMAPIOfflineMgr.](imapiofflinemgrimapioffline.md)** 
  
Член в этом интерфейсе — это замесерв, зарезервированный для внутреннего использования Microsoft Outlook 2013 и на который могут быть внося изменения. Другие члены этого интерфейса должны использоваться только в документе. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

