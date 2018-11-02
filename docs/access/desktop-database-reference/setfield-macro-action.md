---
title: Макрокоманда SetField
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ca2315a9a84000aa29b88043e4edea05ffb0ea
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922827"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="d199b-102">Макрокоманда SetField</span><span class="sxs-lookup"><span data-stu-id="d199b-102">SetField macro action</span></span>


<span data-ttu-id="d199b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d199b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d199b-104">Действие **SetField** используется для присвоения значения поля.</span><span class="sxs-lookup"><span data-stu-id="d199b-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d199b-105"><STRONG>SetField</STRONG> действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="d199b-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="d199b-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="d199b-106">Setting</span></span>

<span data-ttu-id="d199b-107">Действие **SetField** содержит аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d199b-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d199b-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="d199b-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="d199b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d199b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d199b-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="d199b-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d199b-111">Строка, идентифицирующая поле.</span><span class="sxs-lookup"><span data-stu-id="d199b-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d199b-112"><strong>Значение</strong></span><span class="sxs-lookup"><span data-stu-id="d199b-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="d199b-113">Выражение, которое задает значение, задаваемое в поле.</span><span class="sxs-lookup"><span data-stu-id="d199b-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d199b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d199b-114">Remarks</span></span>

<span data-ttu-id="d199b-115">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** .</span><span class="sxs-lookup"><span data-stu-id="d199b-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

