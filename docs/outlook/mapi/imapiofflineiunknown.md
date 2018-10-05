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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401281"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения для автономного объекта.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Запрос на [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Задает текущее состояние автономной объекта в сети или в автономном режиме.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Получает условия, для которых обратные вызовы поддерживаются автономной объектом.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Возвращает текущее состояние сетевым и автономным автономного объекта.  <br/> |
| *Заполнитель члена*  <br/> |Этот член — это и не поддерживается.  <br/> |
   
## <a name="remarks"></a>Замечания

Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получить автономного объекта, который поддерживает **IMAPIOfflineMgr**. Поскольку **IMAPIOfflineMgr** наследуется от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), клиент может запросить этот интерфейс (с помощью [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) для получения указателя на указатель интерфейса для **IMAPIOffline** для автономного объекта. Клиент затем можно получить или задать текущее состояние объекта, или узнать о возможностях обратного вызова объекта (путем вызова **IMAPIOffline::GetCapabilities** ) и выберите Настройка обратных вызовов с помощью **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Член этого интерфейса — это значение зарезервировано для внутреннего использования Microsoft Outlook 2013 и может быть изменен. Другие элементы в этот интерфейс должен использоваться только в документации. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

