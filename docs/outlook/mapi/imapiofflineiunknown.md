---
title: Имапиоффлине IUnknown
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
|Предоставлено:  <br/> |Запрос на [имапиоффлинемгр](imapiofflinemgrimapioffline.md) <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|**[сеткуррентстате](imapioffline-setcurrentstate.md)** <br/> |Задает текущее состояние автономного объекта: Online или offline.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Получает условия, для которых в автономном объекте поддерживаются обратные вызовы.  <br/> |
|**[жеткуррентстате](imapioffline-getcurrentstate.md)** <br/> |Возвращает текущее или автономное состояние автономного объекта.  <br/> |
| *Элемент PlaceHolder*  <br/> |Этот элемент является заполнителем и не поддерживается.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент использует **[хропеноффлинеобж](hropenofflineobj.md)** , чтобы открыть и получить автономный объект, поддерживающий **имапиоффлинемгр**. Так как **имапиоффлинемгр** наследует от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), клиент может запрашивать этот интерфейс (с помощью [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)), чтобы получить указатель на указатель интерфейса для **имапиоффлине** для автономного объекта. Клиент может получить или задать текущее состояние объекта или узнать о возможностях обратного вызова объекта (вызвав **имапиоффлине::-Capabilities** ) и выбрать настройку обратных вызовов с помощью **[имапиоффлинемгр](imapiofflinemgrimapioffline.md)**. 
  
Членом этого интерфейса является заполнитель, зарезервированный для внутреннего использования Microsoft Outlook 2013 и который может быть изменен. Другие члены этого интерфейса должны использоваться только как документально задокументировано. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Интерфейсы MAPI](mapi-interfaces.md)

