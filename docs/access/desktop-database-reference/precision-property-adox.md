---
title: Свойство Precision (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e64a7166b73c5fca1fa7f5e0b63fabeec715c52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927503"
---
# <a name="precision-property-adox"></a><span data-ttu-id="b0a56-102">Свойство Precision (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b0a56-102">Precision property (ADOX)</span></span>


<span data-ttu-id="b0a56-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0a56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0a56-104">Указывает максимальное точность значений данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="b0a56-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b0a56-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b0a56-105">Settings and return values</span></span>

<span data-ttu-id="b0a56-106">Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) является числовым типом.</span><span class="sxs-lookup"><span data-stu-id="b0a56-106">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type.</span></span> <span data-ttu-id="b0a56-107">**Точность** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="b0a56-107">**Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a56-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0a56-108">Remarks</span></span>

<span data-ttu-id="b0a56-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="b0a56-109">The default value is zero (0).</span></span>

<span data-ttu-id="b0a56-110">Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0a56-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

