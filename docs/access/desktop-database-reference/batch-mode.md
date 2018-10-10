---
title: Пакетном режиме (Справочник по для настольных баз данных Access)
TOCTitle: Batch Mode
ms:assetid: b73921f6-5a12-9b26-ea65-99b32dd763f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249883(v=office.15)
ms:contentKeyID: 48547294
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e72997d2484bdfcec91542b0b8de6bbbb23e3fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479938"
---
# <a name="batch-mode"></a><span data-ttu-id="68bda-102">Batch Mode</span><span class="sxs-lookup"><span data-stu-id="68bda-102">Batch Mode</span></span>


<span data-ttu-id="68bda-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="68bda-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="68bda-104">Пакетном режиме — в случае свойство **LockType для** задано значение **adLockBatchOptimistic** и обновление пакета поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="68bda-104">Batch mode is in effect when the **LockType** property is set to **adLockBatchOptimistic** and batch updating is supported by the provider.</span></span> <span data-ttu-id="68bda-105">Некоторые параметры типа блокировки, недоступны в зависимости от расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="68bda-105">Certain lock type settings are not available depending on cursor location.</span></span> <span data-ttu-id="68bda-106">Например тип жесткой блокировки недоступен при **CursorLocation** задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="68bda-106">For instance, a pessimistic lock type is not available when the **CursorLocation** is set to **adUseClient**.</span></span> <span data-ttu-id="68bda-107">И наоборот поставщик может не поддерживать оптимистичный блокировки пакета при положения курсора на сервере.</span><span class="sxs-lookup"><span data-stu-id="68bda-107">Conversely, a provider may not support a batch optimistic lock when the cursor location is on the server.</span></span> <span data-ttu-id="68bda-108">Следует использовать пакетного обновления с набором ключей или статических текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="68bda-108">You should use batch updating with either a keyset or static cursor only.</span></span>

<span data-ttu-id="68bda-109">Метод **UpdateBatch** используется для отправки **записей** изменения, которые проводятся в буфер копирования на сервер, чтобы обновить источник данных.</span><span class="sxs-lookup"><span data-stu-id="68bda-109">The **UpdateBatch** method is used to send **Recordset** changes held in the copy buffer to the server to update the data source.</span></span> <span data-ttu-id="68bda-110">В следующем разделе мы открытия **набора записей** в пакетном режиме, вносить изменения в буфер копирования и отправьте изменения в источник данных, с помощью вызова **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="68bda-110">In the following section, we will open a **Recordset** in batch mode, make changes to the copy buffer, and then send our changes to the data source using a call to **UpdateBatch**.</span></span>

