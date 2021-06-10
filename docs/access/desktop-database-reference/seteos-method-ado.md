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
# <a name="seteos-method-ado"></a><span data-ttu-id="8454a-102">Метод SetEOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="8454a-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="8454a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8454a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8454a-104">Задает позицию, которая является конечным потоком.</span><span class="sxs-lookup"><span data-stu-id="8454a-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8454a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8454a-105">Syntax</span></span>

<span data-ttu-id="8454a-106">*Stream*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="8454a-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="8454a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="8454a-107">Remarks</span></span>

<span data-ttu-id="8454a-108">**SetEOS** обновляет значение свойства [EOS,](eos-property-ado.md) делая текущее [положение](position-property-ado.md) в конце потока.</span><span class="sxs-lookup"><span data-stu-id="8454a-108">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream.</span></span> <span data-ttu-id="8454a-109">Все bytes или characters following the current position are truncated.</span><span class="sxs-lookup"><span data-stu-id="8454a-109">Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="8454a-110">Так как [Write,](write-method-ado.md) [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не усечены дополнительные значения в существующих объектах Stream, вы можете усечь эти bytes или characters, установив новую позицию конечного потока с **SetEOS**. </span><span class="sxs-lookup"><span data-stu-id="8454a-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="8454a-111">Если вы установите **EOS** на позицию до фактического окончания потока, вы потеряете все данные после новой **позиции EOS.**</span><span class="sxs-lookup"><span data-stu-id="8454a-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
