---
title: Глава 8. Общие сведения о курсорах и блокировках
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ff5f62bfaeb182e3399eaa82865fb492853ef30
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861101"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="577c5-102">Глава 8. Общие сведения о курсорах и блокировках</span><span class="sxs-lookup"><span data-stu-id="577c5-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="577c5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="577c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="577c5-104">Важно понять принципы работы курсоры, чтобы вы могли выбрать тип курсора рекомендации и наиболее эффективным для требования доступа к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="577c5-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="577c5-105">Менее чем оптимальную конфигурацию курсора можно сделать еще медленных операций доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="577c5-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="577c5-106">Возможности объект ADO **Recordset** определяется тип и расположение курсора, а также тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="577c5-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="577c5-107">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="577c5-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="577c5-108">Что такое курсор?</span><span class="sxs-lookup"><span data-stu-id="577c5-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

- [<span data-ttu-id="577c5-109">The Significance of Cursor Location</span><span class="sxs-lookup"><span data-stu-id="577c5-109">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

- [<span data-ttu-id="577c5-110">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="577c5-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

- [<span data-ttu-id="577c5-111">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="577c5-111">Using CacheSize</span></span>](using-cachesize.md)

- [<span data-ttu-id="577c5-112">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="577c5-112">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

- [<span data-ttu-id="577c5-113">Types of Cursors (ADO)</span><span class="sxs-lookup"><span data-stu-id="577c5-113">Types of Cursors (ADO)</span></span>](types-of-cursors.md)

- [<span data-ttu-id="577c5-114">What is a Lock? (ADO)</span><span class="sxs-lookup"><span data-stu-id="577c5-114">What is a Lock? (ADO)</span></span>](what-is-a-lock.md)

