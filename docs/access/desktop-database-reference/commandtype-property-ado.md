---
title: CommandType Property (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483237"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="17495-102">CommandType Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="17495-102">CommandType Property (ADO)</span></span>


<span data-ttu-id="17495-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17495-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17495-104">Указывает тип объекта [команды](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="17495-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="17495-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="17495-105">Settings and Return Values</span></span>

<span data-ttu-id="17495-106">Задает или возвращает одно или несколько значений [CommandTypeEnum](commandtypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="17495-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="17495-107">Не используйте значения <STRONG>CommandTypeEnum</STRONG> <STRONG>adCmdFile</STRONG> или <STRONG>adCmdTableDirect</STRONG> с <STRONG>CommandType</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="17495-107">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>.</span></span> <span data-ttu-id="17495-108">Эти значения может использоваться только как параметры методов <A href="open-method-ado-recordset.md">Open</A> и <A href="requery-method-ado.md">повторный запрос</A> набора <A href="recordset-object-ado.md">записей</A>.</span><span class="sxs-lookup"><span data-stu-id="17495-108">These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="17495-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="17495-109">Remarks</span></span>

<span data-ttu-id="17495-110">Используйте свойство **CommandType** для оптимизации оценки свойства [CommandText](commandtext-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="17495-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="17495-111">Если значение свойства **CommandType** равно **adCmdUnknown** (значение по умолчанию), так как ADO необходимо выполнять вызовы к поставщику, чтобы определить свойство **CommandText** инструкции SQL, сохраненного могут возникнуть снижение производительности процедуры, или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="17495-111">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name.</span></span> <span data-ttu-id="17495-112">Если вы знаете, какой тип используется, задав свойство **CommandType** команда указывает ADO для перехода в соответствующий код.</span><span class="sxs-lookup"><span data-stu-id="17495-112">If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code.</span></span> <span data-ttu-id="17495-113">Если свойство **CommandType** не соответствует типу команды в свойстве **CommandText** , возникает ошибка при вызове метода [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="17495-113">If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

