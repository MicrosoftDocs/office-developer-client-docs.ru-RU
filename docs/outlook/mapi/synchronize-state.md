---
title: Синхронизация состояния
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414629"
---
# <a name="synchronize-state"></a>Синхронизация состояния

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описывается, что происходит во время синхронизации состояния машины репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояния:  <br/> |**LR_SYNC** <br/> |
|Связанная структура данных:  <br/> |**[SYNC](sync.md)** <br/> |
|Из этого состояния:  <br/> |[Состояние бездействия](idle-state.md) <br/> |
|Для этого состояния:  <br/> |[Состояние иерархии загрузки,](download-hierarchy-state.md) [синхронизация состояния содержимого,](synchronize-contents-state.md)состояние [иерархии](upload-hierarchy-state.md)загрузки или состояние простоя  <br/> |
   
> [!NOTE]
> Машина состояния репликации — это детерминистический автомат состояния. Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего. 
  
## <a name="description"></a>Описание

Это состояние инициирует синхронизацию. Локальный магазин может перейти на состояние загрузки или загрузки отсюда. Например, локальный магазин может перейти в состояние иерархии отправки для отправки иерархии папок на сервер или выполнить полную синхронизацию, сначала загрузив иерархию, а затем скачав иерархию с сервера.
  
В этом состоянии Outlook инициализирует связанную структуру данных **SYNC** с пути к локальному магазину, чтобы Outlook изменения во время других состояниях. 
  
Клиент задает [в] членов **SYNC**, который Outlook, как обращаться с другими состояниями. Например, клиент может установить *ulFlags* для UPS_UPLOAD_ONLY **и UPS_THESE_FOLDERS**  и прислать в список идентификаторов записей папок, чтобы сообщить Outlook, что будут загружены только эти папки.  Когда это состояние заканчивается, локальный магазин возвращается в состояние простоя. 
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

