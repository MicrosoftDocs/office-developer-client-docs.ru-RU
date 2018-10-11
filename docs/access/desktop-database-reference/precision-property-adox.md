---
title: Precision Property (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fab2a7dc7a2d9f05e22b064acfaeabf93106a3e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480186"
---
# <a name="precision-property-adox"></a><span data-ttu-id="7b8bc-102">Precision Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7b8bc-102">Precision Property (ADOX)</span></span>


<span data-ttu-id="7b8bc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b8bc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7b8bc-104">Указывает максимальное точность значений данных в столбце.</span><span class="sxs-lookup"><span data-stu-id="7b8bc-104">Indicates the maximum precision of data values in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7b8bc-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7b8bc-105">Settings and Return Values</span></span>

<span data-ttu-id="7b8bc-106">Задает и возвращает значение типа **Long** , является максимальной точности значений данных в столбце, если свойство [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) является числовым типом.</span><span class="sxs-lookup"><span data-stu-id="7b8bc-106">Sets and returns a **Long** value that is the maximum precision of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is a numeric type.</span></span> <span data-ttu-id="7b8bc-107">**Точность** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b8bc-107">**Precision** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8bc-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b8bc-108">Remarks</span></span>

<span data-ttu-id="7b8bc-109">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="7b8bc-109">The default value is zero (0).</span></span>

<span data-ttu-id="7b8bc-110">Это свойство доступно только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="7b8bc-110">This property is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

