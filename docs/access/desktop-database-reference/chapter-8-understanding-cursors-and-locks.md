---
title: 'Глава 8: Общее представление о курсоры и блокировки'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ca76b5635e057251aff845ecf45146e6e0d89a6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936942"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="b8137-102">Глава 8: Общее представление о курсоры и блокировки</span><span class="sxs-lookup"><span data-stu-id="b8137-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="b8137-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8137-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8137-104">Важно понять принципы работы курсоры, чтобы вы могли выбрать тип курсора рекомендации и наиболее эффективным для требования доступа к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="b8137-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="b8137-105">Менее чем оптимальную конфигурацию курсора можно сделать еще медленных операций доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="b8137-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="b8137-106">Возможности объект ADO **Recordset** определяется тип и расположение курсора, а также тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="b8137-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="b8137-107">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="b8137-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="b8137-108">Что такое курсор?</span><span class="sxs-lookup"><span data-stu-id="b8137-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="b8137-109">Значение позиции курсора</span><span class="sxs-lookup"><span data-stu-id="b8137-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="b8137-110">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="b8137-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="b8137-111">Использование свойства CacheSize</span><span class="sxs-lookup"><span data-stu-id="b8137-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="b8137-112">Характеристики курсора и блокировки</span><span class="sxs-lookup"><span data-stu-id="b8137-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="b8137-113">Типы курсоров (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8137-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="b8137-114">Что такое блокировки? (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8137-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

