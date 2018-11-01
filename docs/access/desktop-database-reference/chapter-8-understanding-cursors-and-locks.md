---
title: Глава 8. Общие сведения о курсорах и блокировках
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b98952e64eac3c35ed67f50e50776c08e594474
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869087"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="5b65b-102">Глава 8. Общие сведения о курсорах и блокировках</span><span class="sxs-lookup"><span data-stu-id="5b65b-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="5b65b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b65b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b65b-104">Важно понять принципы работы курсоры, чтобы вы могли выбрать тип курсора рекомендации и наиболее эффективным для требования доступа к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="5b65b-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="5b65b-105">Менее чем оптимальную конфигурацию курсора можно сделать еще медленных операций доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="5b65b-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="5b65b-106">Возможности объект ADO **Recordset** определяется тип и расположение курсора, а также тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="5b65b-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="5b65b-107">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="5b65b-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="5b65b-108">Что такое курсор?</span><span class="sxs-lookup"><span data-stu-id="5b65b-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

- [<span data-ttu-id="5b65b-109">The Significance of Cursor Location</span><span class="sxs-lookup"><span data-stu-id="5b65b-109">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

- [<span data-ttu-id="5b65b-110">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="5b65b-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

- [<span data-ttu-id="5b65b-111">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="5b65b-111">Using CacheSize</span></span>](using-cachesize.md)

- [<span data-ttu-id="5b65b-112">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="5b65b-112">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

- [<span data-ttu-id="5b65b-113">Types of Cursors (ADO)</span><span class="sxs-lookup"><span data-stu-id="5b65b-113">Types of Cursors (ADO)</span></span>](types-of-cursors.md)

- [<span data-ttu-id="5b65b-114">What is a Lock? (ADO)</span><span class="sxs-lookup"><span data-stu-id="5b65b-114">What is a Lock? (ADO)</span></span>](what-is-a-lock.md)

