---
title: Type Property (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602743"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="b99b8-102">Type Property (ADO Stream)</span><span class="sxs-lookup"><span data-stu-id="b99b8-102">Type Property (ADO Stream)</span></span>


<span data-ttu-id="b99b8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b99b8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b99b8-104">Указывает тип данных, содержащихся в [потоке](stream-object-ado.md) (двоичный или текст).</span><span class="sxs-lookup"><span data-stu-id="b99b8-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

<span data-ttu-id="b99b8-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b99b8-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="b99b8-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b99b8-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="b99b8-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b99b8-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="b99b8-108">master</span><span class="sxs-lookup"><span data-stu-id="b99b8-108">master</span></span>

<span data-ttu-id="b99b8-109">Задает или возвращает [StreamTypeEnum](streamtypeenum.md) значение, задающее тип данных, содержащихся в объекте **потока** .</span><span class="sxs-lookup"><span data-stu-id="b99b8-109">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object.</span></span> <span data-ttu-id="b99b8-110">Значение по умолчанию — **adTypeText**.</span><span class="sxs-lookup"><span data-stu-id="b99b8-110">The default value is **adTypeText**.</span></span> <span data-ttu-id="b99b8-111">Тем не менее если изначально двоичные данные записываются новый, пустой **поток**, **Тип** будет изменено на **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="b99b8-111">However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b99b8-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="b99b8-112">Remarks</span></span>

<span data-ttu-id="b99b8-113">Является ли данное свойство **Тип** чтения и записи только в том случае, если текущее положение находится в начале **потока** ([положение](position-property-ado.md) — 0) и только для чтения в любом другом месте.</span><span class="sxs-lookup"><span data-stu-id="b99b8-113">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="b99b8-114">Свойство **Type** определяет, какие методы можно использовать для чтения и записи в **поток**.</span><span class="sxs-lookup"><span data-stu-id="b99b8-114">The **Type** property determines which methods should be used for reading and writing the **Stream**.</span></span> <span data-ttu-id="b99b8-115">Для текста, **потоки**используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b99b8-115">For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md).</span></span> <span data-ttu-id="b99b8-116">Для двоичных **потоков**используйте [чтения](read-method-ado.md) и [записи](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b99b8-116">For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

