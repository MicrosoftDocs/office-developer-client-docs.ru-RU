---
title: Именование папок с использованием строк символов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810039"
---
# <a name="naming-folders-by-using-character-strings"></a>Именование папок с использованием строк символов

  
  
**Относится к**: Outlook 
  
Если доступ к одной или нескольких папок часто во время сеанса, рассмотрите возможность назначения имен в папки с помощью метода [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Хотя **IMsgStore::SetReceiveFolder** используется в основном для установления специальные папки для получения входящих сообщений по классам конкретное сообщение, оно также может использоваться для сопоставления любую папку с именем. Имя может совпадать с классом сообщения или она может быть любой строкой, настроенный для использования вашего клиента. Сопоставление имени с папкой снижает время, необходимое для поиска и откройте папку. 
  

