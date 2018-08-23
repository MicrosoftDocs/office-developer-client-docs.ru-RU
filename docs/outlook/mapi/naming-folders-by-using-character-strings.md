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
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594588"
---
# <a name="naming-folders-by-using-character-strings"></a>Именование папок с использованием строк символов

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Если доступ к одной или нескольких папок часто во время сеанса, рассмотрите возможность назначения имен в папки с помощью метода [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Хотя **IMsgStore::SetReceiveFolder** используется в основном для установления специальные папки для получения входящих сообщений по классам конкретное сообщение, оно также может использоваться для сопоставления любую папку с именем. Имя может совпадать с классом сообщения или она может быть любой строкой, настроенный для использования вашего клиента. Сопоставление имени с папкой снижает время, необходимое для поиска и откройте папку. 
  

