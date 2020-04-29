---
title: Имаписинкпрогресскаллбакк IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418339"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Передает поставщик магазина в виде поля в структуре МАПИСИБ во время вызова [имаписинк: синчронизеинбаккграунд](imapisyncsynchronizeinbackground.md). Поставщик магазина использует этот интерфейс для обратной связи с Microsoft Outlook о состоянии синхронизации.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> ||
|Предоставлено:  <br/> |Outlook  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг хранения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |Поставщик хранилища периодически вызывает эту функцию для обновления состояния в диалоговом окне отправки и получения.  <br/> |
|[Ошибка](imapisyncprogresscallback-error.md) <br/> |Если во время синхронизации возникли ошибки, поставщик услуг хранения вызывает эту функцию для предоставления сведений, отображаемых в диалоговом окне отправки и получения.  <br/> |
|[Done](imapisyncprogresscallback-done.md) <br/> |Поставщик услуг Store вызывает эту функцию, чтобы сообщить Outlook о завершении синхронизации.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISync : IUnknown](imapisynciunknown.md)


[Интерфейсы MAPI](mapi-interfaces.md)

