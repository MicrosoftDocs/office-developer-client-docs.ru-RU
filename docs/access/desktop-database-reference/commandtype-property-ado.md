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
localization_priority: Normal
ms.openlocfilehash: c978a6a227266fa43c1102fc109be2b81262de8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296124"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="436ab-102">Свойство CommandType (ADO)</span><span class="sxs-lookup"><span data-stu-id="436ab-102">CommandType property (ADO)</span></span>


<span data-ttu-id="436ab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="436ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="436ab-104">Указывает тип объекта [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="436ab-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="436ab-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="436ab-105">Settings and return values</span></span>

<span data-ttu-id="436ab-106">Задает или возвращает одно или несколько [значений CommandTypeEnum.](commandtypeenum.md)</span><span class="sxs-lookup"><span data-stu-id="436ab-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="436ab-107">Не используйте значения **CommandTypeEnum** **adCmdFile** или **adCmdTableDirect** с **CommandType.**</span><span class="sxs-lookup"><span data-stu-id="436ab-107">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**.</span></span> <span data-ttu-id="436ab-108">Эти значения можно использовать только в качестве параметров с методами [Open](open-method-ado-recordset.md) и [Requery](requery-method-ado.md) для [recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="436ab-108">These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="436ab-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="436ab-109">Remarks</span></span>

<span data-ttu-id="436ab-110">Используйте свойство **CommandType для** оптимизации оценки свойства [CommandText.](commandtext-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="436ab-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="436ab-111">Если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), производительность может снизиться, так как ADO должен звонить поставщику, чтобы определить, является ли свойство **CommandText** оператором SQL, хранимой процедурой или именем таблицы.</span><span class="sxs-lookup"><span data-stu-id="436ab-111">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name.</span></span> <span data-ttu-id="436ab-112">Если вы знаете, какой тип команды вы используете, установка свойства **CommandType** дает ADO указание перейти непосредственно к соответствующему коду.</span><span class="sxs-lookup"><span data-stu-id="436ab-112">If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code.</span></span> <span data-ttu-id="436ab-113">Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText,** при вызове метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="436ab-113">If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

