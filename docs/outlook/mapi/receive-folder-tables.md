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
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812101"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="b9b6e-103">Таблицы папок получения</span><span class="sxs-lookup"><span data-stu-id="b9b6e-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="b9b6e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9b6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9b6e-105">Таблица получения папка содержит сведения для всех папок, обозначены как получения папки для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="b9b6e-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="b9b6e-106">Папка получения является там, где размещены входящих сообщений класса определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b9b6e-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="b9b6e-107">Реализация поставщиков хранилища сообщений принимать папки таблиц и их использовать клиентские приложения путем вызова метода [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="b9b6e-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="b9b6e-108">Следующие свойства составляющих обязательный столбец, задайте получают таблиц папки:</span><span class="sxs-lookup"><span data-stu-id="b9b6e-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="b9b6e-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9b6e-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="b9b6e-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9b6e-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="b9b6e-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9b6e-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9b6e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b9b6e-112">See also</span></span>



[<span data-ttu-id="b9b6e-113">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="b9b6e-113">MAPI Tables</span></span>](mapi-tables.md)

