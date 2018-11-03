---
title: Пакетном режиме (Справочник по для настольных баз данных Access)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9541e8b7888f5fb5f16bcfb343d545cf304b1afd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945791"
---
# <a name="batch-mode"></a><span data-ttu-id="66e9a-102">Пакетном режиме</span><span class="sxs-lookup"><span data-stu-id="66e9a-102">Batch mode</span></span>

<span data-ttu-id="66e9a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66e9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66e9a-104">Пакетном режиме — в случае свойство **LockType для** задано значение **adLockBatchOptimistic** и обновление пакета поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="66e9a-104">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider.</span></span> <span data-ttu-id="66e9a-105">Некоторые параметры типа блокировки, недоступны в зависимости от расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="66e9a-105">Certain lock type settings are not available depending on cursor location.</span></span> <span data-ttu-id="66e9a-106">Например тип жесткой блокировки недоступен при **CursorLocation** задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="66e9a-106">For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**.</span></span> <span data-ttu-id="66e9a-107">И наоборот поставщик может не поддерживать оптимистичный блокировки пакета при положения курсора на сервере.</span><span class="sxs-lookup"><span data-stu-id="66e9a-107">Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server.</span></span> <span data-ttu-id="66e9a-108">Следует использовать пакетного обновления с набором ключей или статических текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="66e9a-108">You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="66e9a-109">Метод **UpdateBatch** используется для отправки **записей** изменения, которые проводятся в буфер копирования на сервер, чтобы обновить источник данных.</span><span class="sxs-lookup"><span data-stu-id="66e9a-109">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source.</span></span> <span data-ttu-id="66e9a-110">В следующем разделе мы открытия **набора записей** в пакетном режиме, вносить изменения в буфер копирования и отправьте изменения в источник данных, с помощью вызова **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="66e9a-110">In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="66e9a-111">В этом разделе содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="66e9a-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="66e9a-112">Отправка обновлений: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="66e9a-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="66e9a-113">Фильтрация для обновленных записей</span><span class="sxs-lookup"><span data-stu-id="66e9a-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="66e9a-114">Работа с ошибками обновлений</span><span class="sxs-lookup"><span data-stu-id="66e9a-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="66e9a-115">Обнаружение и устранение конфликтов</span><span class="sxs-lookup"><span data-stu-id="66e9a-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="66e9a-116">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="66e9a-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="66e9a-117">Обновление результатов Соединяемая: уникальной таблицы</span><span class="sxs-lookup"><span data-stu-id="66e9a-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

