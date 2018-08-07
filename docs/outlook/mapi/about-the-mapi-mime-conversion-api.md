---
title: Сведения об API преобразования MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807985"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Сведения об API преобразования MAPI-MIME

  
  
**Относится к**: Outlook 
  
API преобразования MAPI-MIME позволяет поставщиков почты для преобразования между объектами MIME и сообщения MAPI. Он содержит определения констант, класс идентификаторы и идентификаторы интерфейса, как показано в [Константы MAPI](mapi-constants.md). Поставщики почты должен cocreate экземпляр **[IConverterSession](iconvertersessioniunknown.md)** путем вызова функции **CoCreateInstance** . 
  

