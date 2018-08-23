---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589086"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Механизм синхронизации электронной почты, а не с помощью API транспорта. Этот интерфейс предоставляется на объект хранилища. С помощью этого интерфейса и [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), поставщика транспорта можно обеспечить более хода выполнения и сообщения об ошибках чем, который отображается в диалоговом окне отправки и получения в Microsoft Outlook.
  
Исходящие — это по-прежнему в хранилище по умолчанию. Outlook будет использовать интерфейсов API транспорта для отправки почты, так как исходящее сообщение не может быть внешнего хранилища.
  
|||
|:-----|:-----|
|Предоставляемые:  <br/> |Поставщики хранилища и транспорта  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Вызывается:  <br/> |Поставщики хранилища и транспорта  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |Реализации поставщиками хранилища сообщений. Этот метод вызывается с Outlook 2010 и Outlook 2013, чтобы запустить синхронизацию.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[Интерфейсы MAPI](mapi-interfaces.md)

