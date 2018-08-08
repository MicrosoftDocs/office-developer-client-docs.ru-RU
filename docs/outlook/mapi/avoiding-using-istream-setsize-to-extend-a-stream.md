---
title: Предотвращение использования с помощью IStreamSetSize для расширения потока
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808126"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Расширение потока без использования IStream::SetSize

  
  
**Относится к**: Outlook 
  
При создании потоков, это необходимо увеличить размер, так как их исходный размер больше не достаточно. Используйте метод OLE **IStream::Write** для этого вместо **IStream::SetSize**. **IStream::Write** автоматически расширяет потока, что ** IStream::SetSize ** ненужных. Вызов **IStream::Write** без **IStream::SetSize** может быть до трех раз быстрее, чем внесения **SetSize** звонков до **записи**.
  

