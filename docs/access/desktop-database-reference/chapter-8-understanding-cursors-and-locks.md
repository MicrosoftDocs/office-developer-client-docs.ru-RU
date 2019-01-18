---
title: Глава 8. Курсоры и блокировки
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3075c0c9bd8267f6b30773a846523172eb2ef603
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726094"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="7e3a9-102">Глава 8. Курсоры и блокировки</span><span class="sxs-lookup"><span data-stu-id="7e3a9-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="7e3a9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e3a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e3a9-104">Важно понять принципы работы курсоры, чтобы вы могли выбрать тип курсора рекомендации и наиболее эффективным для требования доступа к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="7e3a9-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="7e3a9-105">Менее чем оптимальную конфигурацию курсора можно сделать еще медленных операций доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="7e3a9-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="7e3a9-106">Возможности объект ADO **Recordset** определяется тип и расположение курсора, а также тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="7e3a9-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="7e3a9-107">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="7e3a9-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="7e3a9-108">Что такое курсор?</span><span class="sxs-lookup"><span data-stu-id="7e3a9-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="7e3a9-109">Значение позиции курсора</span><span class="sxs-lookup"><span data-stu-id="7e3a9-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="7e3a9-110">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="7e3a9-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="7e3a9-111">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="7e3a9-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="7e3a9-112">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="7e3a9-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="7e3a9-113">Типы курсоров (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e3a9-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="7e3a9-114">Что такое блокировки? (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e3a9-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

