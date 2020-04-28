---
title: Пакетный режим (Справочник по базам данных Access на компьютере)
TOCTitle: Batch mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac5f14d035a4e11cce67f01ca6636f3ebd39963e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296880"
---
# <a name="batch-mode"></a><span data-ttu-id="394e0-102">Пакетный режим</span><span class="sxs-lookup"><span data-stu-id="394e0-102">Batch mode</span></span>

<span data-ttu-id="394e0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="394e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="394e0-104">Пакетный режим действует, если для свойства **LockType** задано значение **адлоккбатчоптимистик** , а поставщик поддерживает пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="394e0-104">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider.</span></span> <span data-ttu-id="394e0-105">Некоторые параметры типа блокировки недоступны в зависимости от положения курсора.</span><span class="sxs-lookup"><span data-stu-id="394e0-105">Certain lock type settings are not available depending on cursor location.</span></span> <span data-ttu-id="394e0-106">Например, тип пессимистической блокировки недоступен, если для **CursorLocation** задано значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="394e0-106">For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**.</span></span> <span data-ttu-id="394e0-107">Кроме того, поставщик может не поддерживать оптимистическую блокировку при размещении курсора на сервере.</span><span class="sxs-lookup"><span data-stu-id="394e0-107">Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server.</span></span> <span data-ttu-id="394e0-108">Пакетное обновление следует использовать только с помощью набора ключей или только статического курсора.</span><span class="sxs-lookup"><span data-stu-id="394e0-108">You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="394e0-109">Метод **UpdateBatch** используется для отправки изменений в **наборе записей** , хранящихся в буфере копирования, на сервер для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="394e0-109">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source.</span></span> <span data-ttu-id="394e0-110">В следующем разделе мы отправим **набор записей** в пакетном режиме, вносите изменения в буфер копирования, а затем отправляете изменения в источник данных с помощью вызова **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="394e0-110">In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

<span data-ttu-id="394e0-111">В этой статье содержатся следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="394e0-111">This section includes the following topics:</span></span>

- [<span data-ttu-id="394e0-112">Отправка обновлений: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="394e0-112">Sending the updates: UpdateBatch</span></span>](sending-the-updates-updatebatch.md)
- [<span data-ttu-id="394e0-113">Поиск обновленных записей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="394e0-113">Filtering for updated records</span></span>](filtering-for-updated-records.md)
- [<span data-ttu-id="394e0-114">Исправление неудачных обновлений</span><span class="sxs-lookup"><span data-stu-id="394e0-114">Dealing with failed updates</span></span>](dealing-with-failed-updates.md)
- [<span data-ttu-id="394e0-115">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="394e0-115">Detecting and resolving conflicts</span></span>](detecting-and-resolving-conflicts.md)
- [<span data-ttu-id="394e0-116">Отключение и повторное подключение набора записей</span><span class="sxs-lookup"><span data-stu-id="394e0-116">Disconnecting and reconnecting the Recordset</span></span>](disconnecting-and-reconnecting-the-recordset.md)
- [<span data-ttu-id="394e0-117">Обновление результатов JOINed: уникальная таблица</span><span class="sxs-lookup"><span data-stu-id="394e0-117">Updating JOINed results: Unique Table</span></span>](updating-joined-results-unique-table.md)

