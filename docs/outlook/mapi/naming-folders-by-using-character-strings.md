---
title: Именовать папки с помощью строк символов
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
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="8df77-103">Именовать папки с помощью строк символов</span><span class="sxs-lookup"><span data-stu-id="8df77-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="8df77-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8df77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8df77-105">При частом доступе к одной или несколько папок во время сеанса следует назначить имена в папки методом [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md)</span><span class="sxs-lookup"><span data-stu-id="8df77-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="8df77-106">Хотя **IMsgStore::SetReceiveFolder** используется в основном для создания специальных папок для получения входящих сообщений для определенных классов сообщений, его также можно использовать для связывания любой папки с именем.</span><span class="sxs-lookup"><span data-stu-id="8df77-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="8df77-107">Имя может быть таким же, как класс сообщения, или это может быть любая строка символов, настроенная для использования клиента.</span><span class="sxs-lookup"><span data-stu-id="8df77-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="8df77-108">Связывание имени с папкой уменьшает время, необходимое для поиска и открытия папки.</span><span class="sxs-lookup"><span data-stu-id="8df77-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

