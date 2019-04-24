---
title: Получение и установка свойств с помощью методов GetProps и SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299400"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Получение и установка свойств с помощью методов GetProps и SetProps
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда это возможно, попробуйте получить или изменить свойство с помощью методов [IMAPIProp::](imapiprop-getprops.md) IMAPIProp и [:: SetProps](imapiprop-setprops.md) . Если свойство, с которым вы работаете, слишком велико, эти методы должны быть достаточными. Другой альтернативой является считывание из потока и запись в него с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . Потоки могут успешно обрабатывать очень большие свойства, но они больше очищаются по ресурсам, так как они нуждаются в библиотеках COM. Используйте интерфейс **IStream** только после вызова **IMAPIProp:: PROPS** или **IMAPIProp:: SetProps** не работает. 
  

