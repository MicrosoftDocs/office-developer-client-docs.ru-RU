---
title: RDS Returns "Stream Not Read" Error
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a9b3372db2ff86ea2af401720ba091100d4cfce1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483062"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="e7a7f-102">Возвращает служб удаленных рабочих СТОЛОВ \"не чтения в потоковом режиме\" об ошибках</span><span class="sxs-lookup"><span data-stu-id="e7a7f-102">RDS Returns \"Stream Not Read\" Error</span></span>


<span data-ttu-id="e7a7f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7a7f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e7a7f-104">«Объект Stream не удалось прочитать из-за его пуст, или текущую позицию в конце потока.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-104">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream.</span></span> <span data-ttu-id="e7a7f-105">Для потоков непустые значение текущей позиции со свойством положение.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-105">For non-empty Streams, set the current position with the Position property.</span></span> <span data-ttu-id="e7a7f-106">Чтобы определить, если потока будет пустым, проверьте свойства Size.»</span><span class="sxs-lookup"><span data-stu-id="e7a7f-106">To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="e7a7f-107">Если возникнет ошибка выше, возможно, в результате попытка использовать иерархических параметризованный запрос по протоколу http.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-107">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http.</span></span> <span data-ttu-id="e7a7f-108">Служб удаленных рабочих СТОЛОВ не разрешено удаленного параметризованный иерархии.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-108">RDS does not permit you to remote parameterized hierarchies.</span></span>

