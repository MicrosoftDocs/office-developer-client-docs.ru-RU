---
title: Состояние скачивания данных иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384859"
---
# <a name="download-hierarchy-state"></a>Состояние скачивания данных иерархии

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описываются двоичных файлов состояние иерархии загрузки конечного автомата репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояний:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Структура связанных данных:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Из этого состояния:  <br/> |[Синхронизировать состояние](synchronize-state.md) <br/> |
|Это состояние:  <br/> |Синхронизировать состояние  <br/> |
   
> [!NOTE]
> Конечный автомат репликации является детерминированным конечного автомата. Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний. 
  
## <a name="description"></a>Описание

Это состояние означает инициирует загрузка дерева иерархии папок с сервера в локальном хранилище. 
  
Outlook инициализирует связанной структуры данных **DNHIER** с указатель в иерархию. Клиент загружает иерархии и вставляет новой папки или изменения папок в локальном хранилище. Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS). Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.
  
По окончании этого состояния локального хранилища возвращается в состояние синхронизации.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

