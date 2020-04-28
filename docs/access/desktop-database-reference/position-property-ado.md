---
title: Свойство Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287526"
---
# <a name="position-property-ado"></a><span data-ttu-id="0b937-102">Свойство Position (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b937-102">Position property (ADO)</span></span>

<span data-ttu-id="0b937-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b937-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b937-104">Указывает текущее положение в объекте [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0b937-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0b937-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0b937-105">Settings and return values</span></span>

<span data-ttu-id="0b937-106">Задает или возвращает значение **типа Long** , задающее смещение текущей позиции от начала потока (в байтах).</span><span class="sxs-lookup"><span data-stu-id="0b937-106">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream.</span></span> <span data-ttu-id="0b937-107">Значение по умолчанию — 0, которое представляет первый байт в потоке.</span><span class="sxs-lookup"><span data-stu-id="0b937-107">The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b937-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b937-108">Remarks</span></span>

<span data-ttu-id="0b937-109">Текущая позиция может быть перемещена в точку после завершения потока.</span><span class="sxs-lookup"><span data-stu-id="0b937-109">The current position can be moved to a point after the end of the stream.</span></span> <span data-ttu-id="0b937-110">Если вы укажете текущую позицию за пределами потока, [Размер](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) объекта **Stream** увеличится соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="0b937-110">If you specify the current position beyond the end of the stream, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** object will be increased accordingly.</span></span> <span data-ttu-id="0b937-111">Все новые байты, добавленные таким образом, будут иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="0b937-111">Any new bytes added in this way will be null.</span></span>

> [!NOTE]
> <span data-ttu-id="0b937-112">**Положение** всегда измеряется в байтах.</span><span class="sxs-lookup"><span data-stu-id="0b937-112">**Position** always measures bytes.</span></span> <span data-ttu-id="0b937-113">Для текстовых потоков, использующих многобайтовые кодировки, умножьте позицию на размер символа, чтобы определить номер символа.</span><span class="sxs-lookup"><span data-stu-id="0b937-113">For text streams using multibyte character sets, multiply the position by the character size to determine the character number.</span></span> <span data-ttu-id="0b937-114">Например, для набора двухбайтовых символов первый символ находится в позиции 0, второй символ в позиции 2, третий символ в позиции 4 и т. д.</span><span class="sxs-lookup"><span data-stu-id="0b937-114">For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span>

<span data-ttu-id="0b937-115">Отрицательные значения нельзя использовать для изменения текущей позиции в **потоке**.</span><span class="sxs-lookup"><span data-stu-id="0b937-115">Negative values cannot be used to change the current position in a **Stream**.</span></span> <span data-ttu-id="0b937-116">Для **позиции**можно использовать только положительные числа.</span><span class="sxs-lookup"><span data-stu-id="0b937-116">Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="0b937-117">Для объектов **Stream** , предназначенных только для чтения, ADO не возвращает ошибку, если для **позиции** задано значение, превышающее **Размер** **потока**.</span><span class="sxs-lookup"><span data-stu-id="0b937-117">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="0b937-118">Это не приводит к изменению размера **потока**или изменению содержимого **потока** любым способом.</span><span class="sxs-lookup"><span data-stu-id="0b937-118">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="0b937-119">Тем не менее, следует избегать этого, так как это приводит к бессмысленному значению **позиции** .</span><span class="sxs-lookup"><span data-stu-id="0b937-119">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

