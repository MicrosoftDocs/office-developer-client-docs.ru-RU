---
title: Предотвращение использования Истреамсетсизе для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331642"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Предотвращение использования IStream:: SetSize для расширения потока

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При записи в потоки иногда требуется увеличить их, так как их исходный размер больше не достаточно. Используйте метод OLE **IStream:: Write** , чтобы сделать это, а не **IStream:: SetSize**. **IStream:: запись** автоматически расширяет поток, делая * * IStream:: SetSize * * не требуется. Вызов **IStream:: Write** без **IStream:: SetSize** может выполняться до трех раз быстрее, чем при вызове метода **SetSize** перед **записью**.
  

