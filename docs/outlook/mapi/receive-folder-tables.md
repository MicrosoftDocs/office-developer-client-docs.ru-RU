---
title: Таблицы папок получения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328478"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="bc61e-103">Таблицы папок получения</span><span class="sxs-lookup"><span data-stu-id="bc61e-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="bc61e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc61e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc61e-105">Таблица получить папку содержит сведения обо всех папках, назначенных в качестве папок получения для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc61e-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="bc61e-106">Папка получения — это папка, в которой размещаются входящие сообщения определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc61e-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="bc61e-107">Поставщики хранилищ сообщений реализуют таблицы получения и клиентские приложения используют их, выполнив вызов метода [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="bc61e-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="bc61e-108">Следующие свойства составляют обязательный набор столбцов в таблицах получения папок:</span><span class="sxs-lookup"><span data-stu-id="bc61e-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="bc61e-109">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc61e-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="bc61e-110">**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc61e-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="bc61e-111">**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc61e-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc61e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="bc61e-112">See also</span></span>



[<span data-ttu-id="bc61e-113">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="bc61e-113">MAPI Tables</span></span>](mapi-tables.md)

