---
title: Метод SetEOS (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f3b1ee81928a8da77cc3edff7f1feffb7196bba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308710"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="7ec7d-102">Метод SetEOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="7ec7d-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="7ec7d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ec7d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ec7d-104">Задает положение, которое является окончанием потока.</span><span class="sxs-lookup"><span data-stu-id="7ec7d-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ec7d-105">Syntax</span></span>

<span data-ttu-id="7ec7d-106">*Stream*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="7ec7d-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec7d-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="7ec7d-107">Remarks</span></span>

<span data-ttu-id="7ec7d-108">**SetEOS** обновляет значение свойства [EOS,](eos-property-ado.md) делая [](position-property-ado.md) текущую позицию конечной частью потока.</span><span class="sxs-lookup"><span data-stu-id="7ec7d-108">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream.</span></span> <span data-ttu-id="7ec7d-109">Все bytes или characters following the current position are truncated.</span><span class="sxs-lookup"><span data-stu-id="7ec7d-109">Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="7ec7d-110">Так как [write,](write-method-ado.md) [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не укорачивать дополнительные значения в существующих объектах **Stream,** вы можете усечь эти значения или символы, задав новую позицию конечного потока с **помощью SetEOS.**</span><span class="sxs-lookup"><span data-stu-id="7ec7d-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="7ec7d-111">Если вы установите **для EOS** положение перед фактическим завершением потока, вы потеряете все данные после новой позиции **EOS.**</span><span class="sxs-lookup"><span data-stu-id="7ec7d-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
