---
title: Свойство NumericScale (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1a15f78463ca0ff6e690b600b9cdca7cc194c7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025961"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="5e151-102">Свойство NumericScale (ADOX)</span><span class="sxs-lookup"><span data-stu-id="5e151-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="5e151-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e151-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e151-104">Указывает масштаб числовое значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="5e151-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5e151-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5e151-105">Settings and return values</span></span>

<span data-ttu-id="5e151-106">Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) свойства — **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="5e151-106">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="5e151-107">**NumericScale** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="5e151-107">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e151-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e151-108">Remarks</span></span>

<span data-ttu-id="5e151-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="5e151-109">The default value is zero (0).</span></span>

<span data-ttu-id="5e151-110">**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="5e151-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

