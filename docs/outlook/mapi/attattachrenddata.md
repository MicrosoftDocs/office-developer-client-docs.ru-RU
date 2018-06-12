---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808084"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Применимо к**: Outlook 
  
Атрибут **attAttachRenddata** закодирован структура **RENDDATA** , описывается, как и где вложения отображается в тексте сообщения. Структура **RENDDATA** просто кодируется в потоке TNEF **sizeof(RENDDATA)** байт, начиная с первого элемента структуры **RENDDATA** . Если участник **dwFlags** структура **RENDDATA** имеет значение **MAC_BINARY**, затем данные для следующих вложения хранятся в файлы формата; в противном случае данные вложения кодируются как обычно.
  

