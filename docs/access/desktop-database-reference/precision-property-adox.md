---
title: Свойство точности (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f61359c368202c1820c713f5842eef3102c3f3d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868415"
---
# <a name="precision-property-adox"></a><span data-ttu-id="3bd0b-102">Свойство точности (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3bd0b-102">Precision Property (ADOX)</span></span>


<span data-ttu-id="3bd0b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bd0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bd0b-104">Указывает максимальное точность значений данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3bd0b-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3bd0b-105">Settings and return values</span></span>

<span data-ttu-id="3bd0b-106">Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) является числовым типом.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-106">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type.</span></span> <span data-ttu-id="3bd0b-107">**Точность** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-107">**Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd0b-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3bd0b-108">Remarks</span></span>

<span data-ttu-id="3bd0b-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="3bd0b-109">The default value is zero (0).</span></span>

<span data-ttu-id="3bd0b-110">Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

