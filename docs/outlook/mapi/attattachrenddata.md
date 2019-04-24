---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331915"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Атрибут **аттаттачренддата** кодируется как структура **ренддата** , описывающая способ и место отображения вложения в тексте сообщения. Структура **ренддата** просто кодируется в потоке TNEF как **sizeof (ренддата)** байтов, начиная с первого элемента структуры **ренддата** . Если для элемента **dwFlags** структуры **ренддата** задано значение **мак_бинари**, то данные для следующего вложения хранятся в формате макбинари; в противном случае данные вложения кодируются как обычно.
  

