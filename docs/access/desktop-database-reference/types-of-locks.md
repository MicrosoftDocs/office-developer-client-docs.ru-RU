---
title: Типы блокировок (Справочник по для настольных баз данных Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a104b2ad452cdf8b0688dbc84ca09b90ed08c62
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944916"
---
# <a name="types-of-locks"></a><span data-ttu-id="76c9a-102">Типы блокировки</span><span class="sxs-lookup"><span data-stu-id="76c9a-102">Types of locks</span></span>


<span data-ttu-id="76c9a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76c9a-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="76c9a-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="76c9a-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="76c9a-105">Указывает оптимистичный пакета обновлений.</span><span class="sxs-lookup"><span data-stu-id="76c9a-105">Indicates optimistic batch updates.</span></span> <span data-ttu-id="76c9a-106">Требуется для пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="76c9a-106">Required for batch update mode.</span></span>

<span data-ttu-id="76c9a-107">Многие приложения получить число строк за один раз и затем необходимо принять согласованных обновлений, включая весь набор строк, вставленных, обновлении или удалении.</span><span class="sxs-lookup"><span data-stu-id="76c9a-107">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted.</span></span> <span data-ttu-id="76c9a-108">С помощью пакетного курсоры, только один цикл к серверу требуется, таким образом обновление повышение эффективности работы и уменьшение сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="76c9a-108">With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic.</span></span> <span data-ttu-id="76c9a-109">Использование библиотеки курсора пакета, можно создать статический курсор и затем отключите от источника данных.</span><span class="sxs-lookup"><span data-stu-id="76c9a-109">Using a batch cursor library, you can create a static cursor and then disconnect from the data source.</span></span> <span data-ttu-id="76c9a-110">На этом этапе можно внести изменения в строках и впоследствии повторное подключение и публикация изменений для источника данных в пакете.</span><span class="sxs-lookup"><span data-stu-id="76c9a-110">At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="76c9a-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="76c9a-111">adLockOptimistic</span></span>

<span data-ttu-id="76c9a-112">Указывает, что поставщик использует оптимистичный блокировки — блокировка записи только при вызове метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="76c9a-112">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method.</span></span> <span data-ttu-id="76c9a-113">Это означает, что существует вероятность, что данных может быть изменен другим пользователем с момента вы измените запись и при вызове **Update**, которая создает конфликтов.</span><span class="sxs-lookup"><span data-stu-id="76c9a-113">This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts.</span></span> <span data-ttu-id="76c9a-114">Используйте этот тип блокировки в ситуациях, когда имеются низкой вероятность конфликта имен или где можно легко разрешить конфликты.</span><span class="sxs-lookup"><span data-stu-id="76c9a-114">Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="76c9a-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="76c9a-115">adLockPessimistic</span></span>

<span data-ttu-id="76c9a-116">Указывает, жесткой блокировки, записи по.</span><span class="sxs-lookup"><span data-stu-id="76c9a-116">Indicates pessimistic locking, record by record.</span></span> <span data-ttu-id="76c9a-117">Поставщик выполняет, что является обязательным для обеспечения успешной редактирования записей, как правило, Блокировка записей в источнике данных немедленно до начала редактирования.</span><span class="sxs-lookup"><span data-stu-id="76c9a-117">The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing.</span></span> <span data-ttu-id="76c9a-118">Конечно, это означает, что записи становится недоступной для других пользователей после начала для редактирования, пока не снятия блокировки путем вызова **Update.**</span><span class="sxs-lookup"><span data-stu-id="76c9a-118">Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.**</span></span> <span data-ttu-id="76c9a-119">Этот тип блокировки используется в системе с которой не может позволить чтобы параллельных изменений в данные, такие как в системы резервирования.</span><span class="sxs-lookup"><span data-stu-id="76c9a-119">Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="76c9a-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="76c9a-120">adLockReadOnly</span></span>

<span data-ttu-id="76c9a-121">Указывает записи только для чтения.</span><span class="sxs-lookup"><span data-stu-id="76c9a-121">Indicates read-only records.</span></span> <span data-ttu-id="76c9a-122">Невозможно изменить данные.</span><span class="sxs-lookup"><span data-stu-id="76c9a-122">You cannot alter the data.</span></span> <span data-ttu-id="76c9a-123">Блокировки только для чтения — «быстрый» тип блокировки, так как сервер для обслуживания блокировка записи не требуется.</span><span class="sxs-lookup"><span data-stu-id="76c9a-123">A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="76c9a-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="76c9a-124">adLockUnspecified</span></span>

<span data-ttu-id="76c9a-125">Не указан тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="76c9a-125">Does not specify a type of lock.</span></span>

