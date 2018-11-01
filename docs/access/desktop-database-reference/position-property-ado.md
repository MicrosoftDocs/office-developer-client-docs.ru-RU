---
title: Свойство Position (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1111cdbc0e5a319f1f3431477854c6d38eff20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875408"
---
# <a name="position-property-ado"></a><span data-ttu-id="32b47-102">Свойство Position (ADO)</span><span class="sxs-lookup"><span data-stu-id="32b47-102">Position property (ADO)</span></span>


<span data-ttu-id="32b47-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32b47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32b47-104">Указывает текущую позицию в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="32b47-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="32b47-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="32b47-105">Settings and return values</span></span>

<span data-ttu-id="32b47-106">Задает или возвращает значение типа **Long** , который определяет, в число байтов текущей позиции от начала потока.</span><span class="sxs-lookup"><span data-stu-id="32b47-106">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream.</span></span> <span data-ttu-id="32b47-107">Значение по умолчанию равно 0, который представляет первого байта ответа в потоке.</span><span class="sxs-lookup"><span data-stu-id="32b47-107">The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b47-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="32b47-108">Remarks</span></span>

<span data-ttu-id="32b47-109">Можно перемещать текущей позиции в точку после завершения потока.</span><span class="sxs-lookup"><span data-stu-id="32b47-109">The current position can be moved to a point after the end of the stream.</span></span> <span data-ttu-id="32b47-110">Если указать текущую позицию за пределами потока будет соответствующим образом увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) объекта **потока** .</span><span class="sxs-lookup"><span data-stu-id="32b47-110">If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly.</span></span> <span data-ttu-id="32b47-111">Любой новый байт, добавлены таким способом будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="32b47-111">Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="32b47-112"><STRONG>Положение</STRONG> всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="32b47-112"><STRONG>Position</STRONG> always measures bytes.</span></span> <span data-ttu-id="32b47-113">Для потоков текста с использованием многобайтовой кодировке умножьте положение на размер знаков для определения количества знаков.</span><span class="sxs-lookup"><span data-stu-id="32b47-113">For text streams using multibyte character sets, multiply the position by the character size to determine the character number.</span></span> <span data-ttu-id="32b47-114">Например для набор двухбайтовых знаков первым символом является позиции 0, второй символ в позиции 2, третий символ в позиции 4 и т. д.</span><span class="sxs-lookup"><span data-stu-id="32b47-114">For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="32b47-115">Отрицательные значения не может использоваться для изменения текущего положения в **потоке**.</span><span class="sxs-lookup"><span data-stu-id="32b47-115">Negative values cannot be used to change the current position in a **Stream**.</span></span> <span data-ttu-id="32b47-116">Для **позиции**можно использовать только положительными числами.</span><span class="sxs-lookup"><span data-stu-id="32b47-116">Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="32b47-117">Для объектов **поток** только для чтения ADO не возвращает ошибку, если **положение** присвоено значение больше, чем **размер** **потока**.</span><span class="sxs-lookup"><span data-stu-id="32b47-117">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="32b47-118">Это не изменять размер **потока**, и не изменяет содержимое **потока** никаких уведомлений.</span><span class="sxs-lookup"><span data-stu-id="32b47-118">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="32b47-119">Тем не менее при этом следует избегать, так как это приводит значение не имеет смысла **положение** .</span><span class="sxs-lookup"><span data-stu-id="32b47-119">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

