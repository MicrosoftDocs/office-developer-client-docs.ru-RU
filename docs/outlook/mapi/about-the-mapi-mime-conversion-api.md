---
title: Сведения об API преобразования MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575268"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Сведения об API преобразования MAPI-MIME

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
API преобразования MAPI-MIME позволяет поставщиков почты для преобразования между объектами MIME и сообщения MAPI. Он содержит определения констант, класс идентификаторы и идентификаторы интерфейса, как показано в [Константы MAPI](mapi-constants.md). Поставщики почты должен cocreate экземпляр **[IConverterSession](iconvertersessioniunknown.md)** путем вызова функции **CoCreateInstance** . 
  

