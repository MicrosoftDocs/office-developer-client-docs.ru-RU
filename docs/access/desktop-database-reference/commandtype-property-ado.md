---
title: Свойство CommandType (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880238"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="5631f-102">Свойство CommandType (ADO)</span><span class="sxs-lookup"><span data-stu-id="5631f-102">CommandType property (ADO)</span></span>


<span data-ttu-id="5631f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5631f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5631f-104">Указывает тип объекта [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5631f-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5631f-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5631f-105">Settings and return values</span></span>

<span data-ttu-id="5631f-106">Задает или возвращает одно или несколько значений [CommandTypeEnum](commandtypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="5631f-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="5631f-107">Не используйте значения **CommandTypeEnum** **adCmdFile** или **adCmdTableDirect** с **CommandType**.</span><span class="sxs-lookup"><span data-stu-id="5631f-107">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**.</span></span> <span data-ttu-id="5631f-108">Эти значения может использоваться только как параметры методов [Open](open-method-ado-recordset.md) и [повторный запрос](requery-method-ado.md) набора [записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5631f-108">These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="5631f-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="5631f-109">Remarks</span></span>

<span data-ttu-id="5631f-110">Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5631f-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="5631f-111">Если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), так как ADO необходимо выполнять вызовы к поставщику, чтобы определить свойство **CommandText** инструкции SQL, сохраненного могут возникнуть снижение производительности процедуры, или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="5631f-111">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name.</span></span> <span data-ttu-id="5631f-112">Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код.</span><span class="sxs-lookup"><span data-stu-id="5631f-112">If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code.</span></span> <span data-ttu-id="5631f-113">Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .</span><span class="sxs-lookup"><span data-stu-id="5631f-113">If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

