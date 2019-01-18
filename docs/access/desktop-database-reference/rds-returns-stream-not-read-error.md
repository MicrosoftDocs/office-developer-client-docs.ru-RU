---
title: RDS возвращает ошибку "Поток не прочитан"
TOCTitle: RDS returns "Stream Not Read" error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0f54d8fdc7e37d0ee01f1ffd29c84a6a8ae799
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703757"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="b0aa4-102">Возвращает служб удаленных рабочих СТОЛОВ \"не чтение потока\" об ошибках</span><span class="sxs-lookup"><span data-stu-id="b0aa4-102">RDS returns \"Stream Not Read\" error</span></span>


<span data-ttu-id="b0aa4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0aa4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0aa4-104">«Объект Stream не удалось прочитать из-за его пуст, или текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="b0aa4-104">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream.</span></span> <span data-ttu-id="b0aa4-105">Для потоков непустые значение текущей позиции со свойством положение.</span><span class="sxs-lookup"><span data-stu-id="b0aa4-105">For non-empty Streams, set the current position with the Position property.</span></span> <span data-ttu-id="b0aa4-106">Чтобы определить, если потока будет пустым, проверьте свойства Size.»</span><span class="sxs-lookup"><span data-stu-id="b0aa4-106">To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="b0aa4-107">Если возникнет ошибка выше, возможно, в результате попытка использовать иерархических параметризованный запрос по протоколу http.</span><span class="sxs-lookup"><span data-stu-id="b0aa4-107">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http.</span></span> <span data-ttu-id="b0aa4-108">Служб удаленных рабочих СТОЛОВ не разрешено удаленного параметризованный иерархии.</span><span class="sxs-lookup"><span data-stu-id="b0aa4-108">RDS does not permit you to remote parameterized hierarchies.</span></span>

