---
title: Типы блокировок (справочник по базам данных Access для настольных ПК)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314163"
---
# <a name="types-of-locks"></a><span data-ttu-id="b5aa6-102">Типы блокировок</span><span class="sxs-lookup"><span data-stu-id="b5aa6-102">Types of locks</span></span>


<span data-ttu-id="b5aa6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5aa6-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="b5aa6-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="b5aa6-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="b5aa6-105">Указывает на оптимистичные пакетные обновления.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-105">Indicates optimistic batch updates.</span></span> <span data-ttu-id="b5aa6-106">Требуется для режима пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-106">Required for batch update mode.</span></span>

<span data-ttu-id="b5aa6-107">Многие приложения извлекали несколько строк одновременно, а затем должны делать согласованные обновления, которые включают весь набор строк для вставки, обновления или удаления.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-107">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted.</span></span> <span data-ttu-id="b5aa6-108">При пакетных курсорах требуется только один круговой путь к серверу, что улучшает производительность обновления и снижает сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-108">With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic.</span></span> <span data-ttu-id="b5aa6-109">С помощью пакетной библиотеки курсоров можно создать статический курсор, а затем отключиться от источника данных.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-109">Using a batch cursor library, you can create a static cursor and then disconnect from the data source.</span></span> <span data-ttu-id="b5aa6-110">На этом этапе можно внести изменения в строки, а затем повторно подключить и опубликовать изменения в источнике данных в пакете.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-110">At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="b5aa6-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="b5aa6-111">adLockOptimistic</span></span>

<span data-ttu-id="b5aa6-112">Указывает, что поставщик использует оптимистичную блокировку — блокировку записей только при вызове метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-112">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method.</span></span> <span data-ttu-id="b5aa6-113">Это означает, что существует вероятность того, что данные могут быть изменены другим пользователем между изменением записи и вызовом **Update,** что создает конфликты.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-113">This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts.</span></span> <span data-ttu-id="b5aa6-114">Используйте этот тип блокировки в ситуациях, когда вероятность столкновений низка или конфликты легко разрешены.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-114">Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="b5aa6-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="b5aa6-115">adLockPessimistic</span></span>

<span data-ttu-id="b5aa6-116">Указывает пессимистическую блокировку, запись по записи.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-116">Indicates pessimistic locking, record by record.</span></span> <span data-ttu-id="b5aa6-117">Поставщик делает все необходимое для успешного редактирования записей, обычно блокировка записей в источнике данных непосредственно перед редактированием.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-117">The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing.</span></span> <span data-ttu-id="b5aa6-118">Конечно, это означает, что записи будут недоступны другим пользователям после начала редактирования, пока вы не отпустите блокировку, вызывая **Update.**</span><span class="sxs-lookup"><span data-stu-id="b5aa6-118">Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.**</span></span> <span data-ttu-id="b5aa6-119">Используйте этот тип блокировки в системе, где вы не можете позволить себе одновременно вносить изменения в данные, например в системе резервирования.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-119">Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="b5aa6-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="b5aa6-120">adLockReadOnly</span></span>

<span data-ttu-id="b5aa6-121">Указывает записи только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-121">Indicates read-only records.</span></span> <span data-ttu-id="b5aa6-122">Изменить данные невозможно.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-122">You cannot alter the data.</span></span> <span data-ttu-id="b5aa6-123">Блокировка, доступная только для чтения, является самым быстрым типом блокировки, так как она не требует, чтобы сервер поддерживал блокировку записей.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-123">A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="b5aa6-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="b5aa6-124">adLockUnspecified</span></span>

<span data-ttu-id="b5aa6-125">Не указывает тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="b5aa6-125">Does not specify a type of lock.</span></span>

