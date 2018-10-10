---
title: NumericScale Property (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4229a318c4eb855b86164f02f1075d29a915d718
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482014"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="f03cf-102">NumericScale Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f03cf-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="f03cf-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f03cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f03cf-104">Указывает масштаб числовое значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="f03cf-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f03cf-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f03cf-105">Settings and Return Values</span></span>

<span data-ttu-id="f03cf-106">Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) свойства — **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="f03cf-106">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="f03cf-107">**NumericScale** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="f03cf-107">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="f03cf-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f03cf-108">Remarks</span></span>

<span data-ttu-id="f03cf-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="f03cf-109">The default value is zero (0).</span></span>

<span data-ttu-id="f03cf-110">**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="f03cf-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

