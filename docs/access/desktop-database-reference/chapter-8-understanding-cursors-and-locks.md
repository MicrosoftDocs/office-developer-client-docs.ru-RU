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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296418"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="da47a-102">Глава 8. Курсоры и блокировки</span><span class="sxs-lookup"><span data-stu-id="da47a-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="da47a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da47a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="da47a-104">Важно понимать, как работают курсоры, чтобы можно было выбрать оптимальный и эффективный тип курсора для требований к доступу к данным приложения.</span><span class="sxs-lookup"><span data-stu-id="da47a-104">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements.</span></span> <span data-ttu-id="da47a-105">Не оптимальная конфигурация курсора может привести к болезненному замедлению операций по доступу к данным.</span><span class="sxs-lookup"><span data-stu-id="da47a-105">A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="da47a-106">Многие возможности объекта ADO **Recordset** определяются типом и расположением курсора, а также типом блокировки.</span><span class="sxs-lookup"><span data-stu-id="da47a-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="da47a-107">В этой главе освещают следующие темы:</span><span class="sxs-lookup"><span data-stu-id="da47a-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="da47a-108">Что такое курсор?</span><span class="sxs-lookup"><span data-stu-id="da47a-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="da47a-109">Значение расположения курсора</span><span class="sxs-lookup"><span data-stu-id="da47a-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="da47a-110">The Microsoft Cursor Service for OLE DB</span><span class="sxs-lookup"><span data-stu-id="da47a-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="da47a-111">Using CacheSize</span><span class="sxs-lookup"><span data-stu-id="da47a-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="da47a-112">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="da47a-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="da47a-113">Типы курсоров (ADO)</span><span class="sxs-lookup"><span data-stu-id="da47a-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="da47a-114">Что такое блокировка? (ADO)</span><span class="sxs-lookup"><span data-stu-id="da47a-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

