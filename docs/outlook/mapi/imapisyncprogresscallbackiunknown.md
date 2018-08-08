---
title: IMAPISyncProgressCallback IUnknown
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
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809195"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**Относится к**: Outlook 
  
Передает поставщика хранилища в качестве поля в структуре MAPISIB во время звонка на [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md). Поставщик хранения использует этот интерфейс для Поделитесь своими впечатлениями о ходе выполнения синхронизации с Microsoft Outlook.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> ||
|Предоставляемые:  <br/> |Outlook  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Вызывается:  <br/> |Поставщики хранилища  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Ход выполнения](imapisyncprogresscallback-progress.md) <br/> |Поставщик хранения периодически вызывает эту функцию для обновления состояния в диалоговом окне отправки и получения.  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |Ошибки, возникающие во время синхронизации, поставщик хранения вызывает эту функцию для предоставления сведений, которые отображаются в диалоговом окне отправки и получения.  <br/> |
|[Договорились](imapisyncprogresscallback-done.md) <br/> |Поставщик хранения вызывает эту функцию для оповещения Outlook, синхронизация завершена.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISync : IUnknown](imapisynciunknown.md)


[Интерфейсы MAPI](mapi-interfaces.md)

