---
title: Сортировка таблиц после установки столбцов и ограничений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409883"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a>Сортировка таблиц после установки столбцов и ограничений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если необходимо ограничить представление отсортированной таблицы, всегда сделайте следующие вызовы **IMAPITable** в следующем порядке: 
  
1. [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
2. [IMAPITable:: restrict](imapitable-restrict.md) to применить ограничение. 
    
3. [IMAPITable:: сорттабле](imapitable-sorttable.md) для выполнения сортировки. 
    
Если таблица отсортирована по категориям, выполните вызов [IMAPITable:: сетколлапсестате](imapitable-setcollapsestate.md), если это необходимо, после вызова **сорттабле** . Этот порядок вызовов важен, так как большинство поставщиков услуг сортируют таблицу в качестве последней задачи для достижения максимальной производительности. Если, например, поставщик хранилища сообщений должен классифицировать таблицу содержимого папки перед настройкой ограничения, эта классификация будет удалена во время обработки ограничения. Необходимо указать вторую классификацию. 
  

