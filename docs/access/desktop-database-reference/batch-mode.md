---
title: Пакетном режиме (Справочник по для настольных баз данных Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717813"
---
# <a name="batch-mode"></a><span data-ttu-id="2b7cd-102">Пакетный режим</span><span class="sxs-lookup"><span data-stu-id="2b7cd-102">Batch mode</span></span>

<span data-ttu-id="2b7cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b7cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b7cd-104">Пакетном режиме — в случае свойство **LockType для** задано значение **adLockBatchOptimistic** и обновление пакета поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-104">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider.</span></span> <span data-ttu-id="2b7cd-105">Некоторые параметры типа блокировки, недоступны в зависимости от расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-105">Certain lock type settings are not available depending on cursor location.</span></span> <span data-ttu-id="2b7cd-106">Например тип жесткой блокировки недоступен при **CursorLocation** задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-106">For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**.</span></span> <span data-ttu-id="2b7cd-107">И наоборот поставщик может не поддерживать оптимистичный блокировки пакета при положения курсора на сервере.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-107">Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server.</span></span> <span data-ttu-id="2b7cd-108">Следует использовать пакетного обновления с набором ключей или статических текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-108">You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="2b7cd-109">Метод **UpdateBatch** используется для отправки **записей** изменения, которые проводятся в буфер копирования на сервер, чтобы обновить источник данных.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-109">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source.</span></span> <span data-ttu-id="2b7cd-110">В следующем разделе мы открытия **набора записей** в пакетном режиме, вносить изменения в буфер копирования и отправьте изменения в источник данных, с помощью вызова **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="2b7cd-110">In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="2b7cd-111">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="2b7cd-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="2b7cd-112">Отправка обновлений: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="2b7cd-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="2b7cd-113">Поиск обновленных записей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="2b7cd-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="2b7cd-114">Исправление неудачных обновлений</span><span class="sxs-lookup"><span data-stu-id="2b7cd-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="2b7cd-115">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="2b7cd-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="2b7cd-116">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="2b7cd-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="2b7cd-117">Обновление результатов JOINed: уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="2b7cd-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

