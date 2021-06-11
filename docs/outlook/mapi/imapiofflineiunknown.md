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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения для автономного объекта.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Запрос [на IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Задает текущее состояние автономного объекта в режиме online или автономном режиме.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Получает условия, для которых вызовы поддерживаются автономным объектом.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Получает текущее состояние автономного объекта в Интернете или автономном режиме.  <br/> |
| *Член placeholder*  <br/> |Этот член является задатщиком и не поддерживается.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получения автономного объекта, поддерживаюшего **IMAPIOfflineMgr.** Поскольку **IMAPIOfflineMgr** наследует [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)клиент может запрашивать этот интерфейс (с помощью [IUnknown::QueryInterface),](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)чтобы получить указатель на указатель интерфейса **для IMAPIOffline** для автономного объекта. Клиент может получить или установить текущее состояние объекта или узнать о возможностях вызова объекта (позвонив **по IMAPIOffline::GetCapabilities)** и выбрать возможность настроить вызовы с помощью **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Член этого интерфейса — это местообладатель, зарезервированный для внутреннего Microsoft Outlook 2013 и подлежит изменениям. Другие участники этого интерфейса должны использоваться только в качестве документированных документов. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

