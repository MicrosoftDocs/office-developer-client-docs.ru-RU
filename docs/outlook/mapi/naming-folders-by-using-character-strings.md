---
title: Именование папок с помощью символьных строк
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326252"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="44458-103">Именование папок с помощью символьных строк</span><span class="sxs-lookup"><span data-stu-id="44458-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="44458-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44458-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44458-105">При частом доступе к одной или нескольким папкам в ходе сеанса рекомендуется назначать имена папкам с помощью метода [IMsgStore:: сетрецеивефолдер](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="44458-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="44458-106">Несмотря на то, что **IMsgStore:: сетрецеивефолдер** используется преимущественно для создания специальных папок для получения входящих сообщений для определенных классов сообщений, он также может использоваться для сопоставления любой папки с именем.</span><span class="sxs-lookup"><span data-stu-id="44458-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="44458-107">Имя может совпадать с классом Message или может представлять собой любую строку символов, настроенную для использования клиента.</span><span class="sxs-lookup"><span data-stu-id="44458-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="44458-108">Связывание имени с папкой сокращает время, необходимое для поиска и открытия папки.</span><span class="sxs-lookup"><span data-stu-id="44458-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

