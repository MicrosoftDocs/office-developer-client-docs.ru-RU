---
title: Именование папок с помощью строк символов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810039"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="4ae7a-103">Именование папок с помощью строк символов</span><span class="sxs-lookup"><span data-stu-id="4ae7a-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="4ae7a-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ae7a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ae7a-105">Если доступ к одной или нескольких папок часто во время сеанса, рассмотрите возможность назначения имен в папки с помощью метода [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae7a-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="4ae7a-106">Хотя **IMsgStore::SetReceiveFolder** используется в основном для установления специальные папки для получения входящих сообщений по классам конкретное сообщение, оно также может использоваться для сопоставления любую папку с именем.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="4ae7a-107">Имя может совпадать с классом сообщения или она может быть любой строкой, настроенный для использования вашего клиента.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="4ae7a-108">Сопоставление имени с папкой снижает время, необходимое для поиска и откройте папку.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

