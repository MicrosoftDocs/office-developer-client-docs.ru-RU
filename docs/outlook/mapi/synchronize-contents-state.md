---
title: Синхронизация состояния содержимого
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438472"
---
# <a name="synchronize-contents-state"></a>Синхронизация состояния содержимого

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описывается, что происходит во время синхронизации состояния содержимого машины состояния репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояния:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Связанная структура данных:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Из этого состояния:  <br/> |[Состояние синхронизации](synchronize-state.md) <br/> |
|Для этого состояния:  <br/> |[Скачивание состояния таблицы,](download-table-state.md) [состояние таблицы](upload-table-state.md)загрузки или синхронизация  <br/> |
   
> [!NOTE]
> Машина состояния репликации — это детерминистический автомат состояния. Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего. 
  
## <a name="description"></a>Описание

Это состояние инициирует один из двух процессов репликации: загрузку содержимого указанных папок в локальном магазине или полную синхронизацию. В полной синхронизации для каждой из указанных папок сначала загружается содержимое, а затем загружается. В зависимости от *ulFlags,* задающихся в соответствующей структуре **[SYNC](sync.md)** в предыдущем состоянии синхронизации, Outlook инициализирует [выход] членов в структуре **SYNCCONT** для предоставления сведений о содержимом. 
  
Через ту же **структуру SYNCCONT** клиент получает количество папок, которые должны быть загружены или загружены. Клиент будет проходить цикл через каждую из этих папок, перемещая локальный магазин в состояние таблицы загрузки для загрузки папки или перемещая локальный магазин в состояние таблицы загрузки для загрузки папки. 
  
Кроме того, клиент получает ID-записи для папок, требующих репликации.
  
Когда это состояние заканчивается, Outlook очищает внутреннюю информацию. Локальный магазин возвращается в состояние синхронизации.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

