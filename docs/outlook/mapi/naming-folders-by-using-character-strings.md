---
title: Именовка папок с помощью строк символов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428314"
---
# <a name="naming-folders-by-using-character-strings"></a>Именовка папок с помощью строк символов

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При частом доступе к одной или более папок во время сеанса можно назначить имена папок с помощью метода [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md) Хотя **IMsgStore::SetReceiveFolder** в основном используется для создания специальных папок для получения входящих сообщений для определенных классов сообщений, его также можно использовать для связывания любой папки с именем. Имя может быть таким же, как класс сообщения, или любой строкой символов, настроенной для использования клиентом. Связывание имени с папкой сокращает время, необходимое для поиска и открытия папки. 
  

