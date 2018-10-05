---
title: Получение и задание свойств с помощью GetProps и SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395009"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Получение и задание свойств с помощью GetProps и SetProps
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Когда это возможно, попробуйте для извлечения или изменения свойства с помощью методов [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::SetProps](imapiprop-setprops.md) . Если свойство, с которым вы работаете с очень большой, должно быть достаточно эти методы. Альтернативой является чтение или запись к потоку с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . Потоки, может обрабатывать очень большой свойства успешно, но они являются более высокой версии затрат на ресурсы, так как они требуют библиотеки COM. С помощью интерфейса **IStream** только после сбоя при вызове **IMAPIProp::GetProps** или **IMAPIProp::SetProps** . 
  

