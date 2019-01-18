---
title: Свойство Type (ADO потока)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721957"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="6ec6e-102">Свойство Type (Stream в ADO)</span><span class="sxs-lookup"><span data-stu-id="6ec6e-102">Type property (ADO Stream)</span></span>


<span data-ttu-id="6ec6e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ec6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ec6e-104">Указывает тип данных, содержащихся в [потоке](stream-object-ado.md) (двоичный или текст).</span><span class="sxs-lookup"><span data-stu-id="6ec6e-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6ec6e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6ec6e-105">Settings and return values</span></span>

<span data-ttu-id="6ec6e-106">Задает или возвращает [StreamTypeEnum](streamtypeenum.md) значение, задающее тип данных, содержащихся в объекте **потока** .</span><span class="sxs-lookup"><span data-stu-id="6ec6e-106">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object.</span></span> <span data-ttu-id="6ec6e-107">Значение по умолчанию — **adTypeText**.</span><span class="sxs-lookup"><span data-stu-id="6ec6e-107">The default value is **adTypeText**.</span></span> <span data-ttu-id="6ec6e-108">Тем не менее если изначально двоичные данные записываются новый, пустой **поток**, **Тип** будет изменено на **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="6ec6e-108">However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec6e-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ec6e-109">Remarks</span></span>

<span data-ttu-id="6ec6e-110">Является ли данное свойство **Тип** чтения и записи только в том случае, если текущее положение находится в начале **потока** ([положение](position-property-ado.md) — 0) и только для чтения в любом другом месте.</span><span class="sxs-lookup"><span data-stu-id="6ec6e-110">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="6ec6e-111">Свойство **Type** определяет, какие методы можно использовать для чтения и записи в **поток**.</span><span class="sxs-lookup"><span data-stu-id="6ec6e-111">The **Type** property determines which methods should be used for reading and writing the **Stream**.</span></span> <span data-ttu-id="6ec6e-112">Для текста, **потоки**используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6ec6e-112">For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md).</span></span> <span data-ttu-id="6ec6e-113">Для двоичных **потоков**используйте [чтения](read-method-ado.md) и [записи](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6ec6e-113">For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

