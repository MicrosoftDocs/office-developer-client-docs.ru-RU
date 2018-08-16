---
title: Состояние скачивания данных таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808350"
---
# <a name="download-table-state"></a>Состояние скачивания данных таблицы

  
  
**Относится к**: Outlook 
  
 В этом разделе описываются двоичных файлов состояния в таблице загрузки конечного автомата репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояний:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Структура связанных данных:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Из этого состояния:  <br/> |[Синхронизировать состояние содержимого](synchronize-contents-state.md) <br/> |
|Это состояние:  <br/> |Синхронизировать состояние содержимого  <br/> |
   
> [!NOTE]
> Конечный автомат репликации является детерминированным конечного автомата. Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний. 
  
## <a name="description"></a>Описание

Это состояние означает инициирует загрузку в папку. В этом состоянии Outlook инициализирует связанной структуры данных **DNTBL** со сведениями о папке. Клиент файлы для загрузки содержимого папки и обновляет к папке на локальном хранилище с новой содержимое, изменения или удаления с сервера. Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.
  
По окончании этого состояния локального хранилища возвращается в состояние содержимое синхронизировать.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)
