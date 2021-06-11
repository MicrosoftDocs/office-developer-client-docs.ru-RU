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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427138"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Атрибут **attAttachRenddata** закодирован как структура **RENDDATA,** которая описывает, как и где отрисовка вложения в тексте сообщения. Структура **RENDDATA** просто закодирована в потоке TNEF в качестве **bytes sizeof (RENDDATA)** начиная с первого члена структуры **RENDDATA.** Если значение члена **dwFlags** структуры **RENDDATA** задано **MAC_BINARY,** то данные для следующего вложения хранятся в формате MacBinary; в противном случае данные вложения закодируются в обычном режиме.
  

