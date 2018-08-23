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
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569451"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Атрибут **attAttachRenddata** закодирован структура **RENDDATA** , описывается, как и где вложения отображается в тексте сообщения. Структура **RENDDATA** просто кодируется в потоке TNEF **sizeof(RENDDATA)** байт, начиная с первого элемента структуры **RENDDATA** . Если участник **dwFlags** структура **RENDDATA** имеет значение **MAC_BINARY**, затем данные для следующих вложения хранятся в файлы формата; в противном случае данные вложения кодируются как обычно.
  

