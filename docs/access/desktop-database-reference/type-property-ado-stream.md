---
title: Type Property (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bb4cebdb8b4aff1413ec60fe4ebb1e05931f6476
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306253"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="4742a-102">Свойство Type (Stream в ADO)</span><span class="sxs-lookup"><span data-stu-id="4742a-102">Type property (ADO Stream)</span></span>


<span data-ttu-id="4742a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4742a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4742a-104">Указывает тип данных, которые хранятся в [потоке](stream-object-ado.md) (двоичный или текстовый).</span><span class="sxs-lookup"><span data-stu-id="4742a-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4742a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4742a-105">Settings and return values</span></span>

<span data-ttu-id="4742a-106">Задает или возвращает значение [стреамтипинум](streamtypeenum.md) , задающее тип данных, которые хранятся в объекте **Stream** .</span><span class="sxs-lookup"><span data-stu-id="4742a-106">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object.</span></span> <span data-ttu-id="4742a-107">Значение по умолчанию — **адтипетекст**.</span><span class="sxs-lookup"><span data-stu-id="4742a-107">The default value is **adTypeText**.</span></span> <span data-ttu-id="4742a-108">Тем не менее, если двоичные данные изначально записываются в новый пустой **поток**, **Тип** изменится на **адтипебинари**.</span><span class="sxs-lookup"><span data-stu-id="4742a-108">However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4742a-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4742a-109">Remarks</span></span>

<span data-ttu-id="4742a-110">Свойство **Type** доступно для чтения и записи, только когда текущая позиция находится в начале **потока** ([position](position-property-ado.md) равно 0) и доступна только для чтения в любой другой позиции.</span><span class="sxs-lookup"><span data-stu-id="4742a-110">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="4742a-111">Свойство **Type** определяет методы, которые следует использовать для чтения и записи **потока**.</span><span class="sxs-lookup"><span data-stu-id="4742a-111">The **Type** property determines which methods should be used for reading and writing the **Stream**.</span></span> <span data-ttu-id="4742a-112">Для текстовых **потоков**используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4742a-112">For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md).</span></span> <span data-ttu-id="4742a-113">Для двоичных **потоков**используйте разрешение " [Чтение](read-method-ado.md) и [запись](write-method-ado.md)".</span><span class="sxs-lookup"><span data-stu-id="4742a-113">For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

