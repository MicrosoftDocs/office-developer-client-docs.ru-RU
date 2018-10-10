---
title: 'Chapter 8: Understanding Cursors and Locks'
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f363522874f01268f4c1a64515bf6f2cdd6336
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480730"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="0c016-102">Chapter 8: Understanding Cursors and Locks</span><span class="sxs-lookup"><span data-stu-id="0c016-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="0c016-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c016-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0c016-104">Важно понять принципы работы курсоры, чтобы вы могли выбрать тип курсора рекомендации и наиболее эффективным для требования доступа к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="0c016-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="0c016-105">Менее чем оптимальную конфигурацию курсора можно сделать еще медленных операций доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="0c016-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="0c016-106">Возможности объект ADO **Recordset** определяется тип и расположение курсора, а также тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="0c016-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="0c016-107">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="0c016-107">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="0c016-108">What is a Cursor?</span><span class="sxs-lookup"><span data-stu-id="0c016-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

  - [<span data-ttu-id="0c016-109">Types of Cursors</span><span class="sxs-lookup"><span data-stu-id="0c016-109">Types of Cursors</span></span>](types-of-cursors.md)

  - [<span data-ttu-id="0c016-110">The Significance of Cursor Location</span><span class="sxs-lookup"><span data-stu-id="0c016-110">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

  - [<span data-ttu-id="0c016-111">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="0c016-111">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

  - [<span data-ttu-id="0c016-112">What is a Lock?</span><span class="sxs-lookup"><span data-stu-id="0c016-112">What is a Lock?</span></span>](what-is-a-lock.md)

  - [<span data-ttu-id="0c016-113">Using CacheSize</span><span class="sxs-lookup"><span data-stu-id="0c016-113">Using CacheSize</span></span>](using-cachesize.md)

  - [<span data-ttu-id="0c016-114">Cursor and Lock Characteristics</span><span class="sxs-lookup"><span data-stu-id="0c016-114">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

