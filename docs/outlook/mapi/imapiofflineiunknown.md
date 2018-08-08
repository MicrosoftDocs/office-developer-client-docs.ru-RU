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
ms.openlocfilehash: 6f17e501a90a50a4984cae470d3924205c78a604
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809014"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Относится к**: Outlook 
  
Предоставляет сведения для автономного объекта.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Запрос на [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Задает текущее состояние автономной объекта в сети или в автономном режиме.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Получает условия, для которых обратные вызовы поддерживаются автономной объектом.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Возвращает текущее состояние сетевым и автономным автономного объекта.  <br/> |
| *Заполнитель члена*  <br/> |Этот член — это и не поддерживается.  <br/> |
   
## <a name="remarks"></a>Замечания

Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получить автономного объекта, который поддерживает **IMAPIOfflineMgr**. Поскольку **IMAPIOfflineMgr** наследуется от [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx), клиент может запросить этот интерфейс (с помощью [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)) для получения указателя на указатель интерфейса для **IMAPIOffline** для автономного объекта. Клиент затем можно получить или задать текущее состояние объекта, или узнать о возможностях обратного вызова объекта (путем вызова **IMAPIOffline::GetCapabilities** ) и выберите Настройка обратных вызовов с помощью **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Член этого интерфейса — это значение зарезервировано для внутреннего использования Microsoft Outlook 2013 и может быть изменен. Другие элементы в этот интерфейс должен использоваться только в документации. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

