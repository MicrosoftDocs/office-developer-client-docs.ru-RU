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
# <a name="type-property-ado-stream"></a><span data-ttu-id="1d54c-102">Свойство Type (Stream в ADO)</span><span class="sxs-lookup"><span data-stu-id="1d54c-102">Type property (ADO Stream)</span></span>


<span data-ttu-id="1d54c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d54c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d54c-104">Указывает тип данных, содержащихся в [Потоке](stream-object-ado.md) (двоичный или текстовый).</span><span class="sxs-lookup"><span data-stu-id="1d54c-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1d54c-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="1d54c-105">Settings and return values</span></span>

<span data-ttu-id="1d54c-106">Задает или возвращает значение [StreamTypeEnum,](streamtypeenum.md) которое указывает тип данных, содержащихся в **объекте Stream.**</span><span class="sxs-lookup"><span data-stu-id="1d54c-106">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object.</span></span> <span data-ttu-id="1d54c-107">По умолчанию значение **adTypeText**.</span><span class="sxs-lookup"><span data-stu-id="1d54c-107">The default value is **adTypeText**.</span></span> <span data-ttu-id="1d54c-108">Однако если двоичные данные изначально записаны в новый пустой **поток,** **тип** будет изменен на **adTypeBinary.**</span><span class="sxs-lookup"><span data-stu-id="1d54c-108">However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d54c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d54c-109">Remarks</span></span>

<span data-ttu-id="1d54c-110">Свойство **Type** считыв или записываю только в [](position-property-ado.md) том случае, если текущее положение находится в начале потока **(положение** 0) и только для чтения в любом другом расположении.</span><span class="sxs-lookup"><span data-stu-id="1d54c-110">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="1d54c-111">Свойство **Type** определяет, какие методы следует использовать для чтения и записи **потока.**</span><span class="sxs-lookup"><span data-stu-id="1d54c-111">The **Type** property determines which methods should be used for reading and writing the **Stream**.</span></span> <span data-ttu-id="1d54c-112">Для **текстовых Потоки** используйте [ReadText](readtext-method-ado.md) и [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1d54c-112">For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md).</span></span> <span data-ttu-id="1d54c-113">Для двоичных **Потоки** используйте [чтение](read-method-ado.md) и [записи](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1d54c-113">For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

