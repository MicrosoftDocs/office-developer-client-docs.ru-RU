---
title: NumericScale Property (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8cc48c2f5b2b7cc58d21890435f0d959ad1e414
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605872"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="44bf1-102">NumericScale Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="44bf1-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="44bf1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="44bf1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="44bf1-104">Указывает масштаб числовое значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="44bf1-104">Indicates the scale of a numeric value in the column.</span></span>

<span data-ttu-id="44bf1-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="44bf1-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="44bf1-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="44bf1-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="44bf1-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="44bf1-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="44bf1-108">master</span><span class="sxs-lookup"><span data-stu-id="44bf1-108">master</span></span>

<span data-ttu-id="44bf1-109">Задает и возвращает значение в **байтах** , масштаб значений данных в столбце, когда [Тип](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) свойства — **adNumeric** или **adDecimal**.</span><span class="sxs-lookup"><span data-stu-id="44bf1-109">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**.</span></span> <span data-ttu-id="44bf1-110">**NumericScale** игнорируется для всех остальных типов данных.</span><span class="sxs-lookup"><span data-stu-id="44bf1-110">**NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="44bf1-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="44bf1-111">Remarks</span></span>

<span data-ttu-id="44bf1-112">Значение по умолчанию — нуль (0).</span><span class="sxs-lookup"><span data-stu-id="44bf1-112">The default value is zero (0).</span></span>

<span data-ttu-id="44bf1-113">**NumericScale** доступен только для чтения для объектов [столбца](column-object-adox.md) уже добавляется в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="44bf1-113">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

