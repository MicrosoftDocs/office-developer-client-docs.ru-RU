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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722762"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="9335e-102">Метод SetEOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="9335e-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="9335e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9335e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9335e-104">Задает позицию за конец потока.</span><span class="sxs-lookup"><span data-stu-id="9335e-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9335e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9335e-105">Syntax</span></span>

<span data-ttu-id="9335e-106">*Поток*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="9335e-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="9335e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9335e-107">Remarks</span></span>

<span data-ttu-id="9335e-108">**SetEOS** обновляет значение свойства [EOS](eos-property-ado.md) , сделав текущую [позицию](position-property-ado.md) в конец потока.</span><span class="sxs-lookup"><span data-stu-id="9335e-108">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream.</span></span> <span data-ttu-id="9335e-109">Любой байт или после текущего положения знаков усекаются.</span><span class="sxs-lookup"><span data-stu-id="9335e-109">Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="9335e-110">С момента [написания](write-method-ado.md), [WriteText](writetext-method-ado.md)и [CopyTo](copyto-method-ado.md) не удалять любые дополнительные значения в существующие объекты **потока** , задав новое место окончания потока с **SetEOS**можно усекать этих байт или символов.</span><span class="sxs-lookup"><span data-stu-id="9335e-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="9335e-111">Если значение **EOS** позицию перед фактический конец потока, будут потеряны все данные после новую позицию **EOS** .</span><span class="sxs-lookup"><span data-stu-id="9335e-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
