---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11696e379fe618f07a6087eee26ba21a2d27b3e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890920"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="245b0-102">Свойство NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="245b0-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="245b0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="245b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="245b0-104">Указывает масштаб числовое значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="245b0-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="245b0-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="245b0-105">Settings and return values</span></span>

<span data-ttu-id="245b0-106">Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) свойства — **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="245b0-106">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="245b0-107">**NumericScale** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="245b0-107">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="245b0-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="245b0-108">Remarks</span></span>

<span data-ttu-id="245b0-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="245b0-109">The default value is zero (0).</span></span>

<span data-ttu-id="245b0-110">**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="245b0-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

