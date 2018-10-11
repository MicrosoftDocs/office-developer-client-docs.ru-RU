---
title: SetField Macro Action
TOCTitle: SetField Macro Action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7050065ccb42d5e6cc9347f32df056891f4ed078
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482077"
---
# <a name="setfield-macro-action"></a><span data-ttu-id="f1c75-102">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="f1c75-102">SetField Macro Action</span></span>


<span data-ttu-id="f1c75-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1c75-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f1c75-104">Действие **SetField** используется для присвоения значения поля.</span><span class="sxs-lookup"><span data-stu-id="f1c75-104">The **SetField** action can be used to assign a value to a field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f1c75-105"><STRONG>SetField</STRONG> действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="f1c75-105">The <STRONG>SetField</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="f1c75-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1c75-106">Setting</span></span>

<span data-ttu-id="f1c75-107">Действие **SetField** содержит аргументы, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f1c75-107">The **SetField** action has the arguments listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1c75-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="f1c75-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="f1c75-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f1c75-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1c75-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="f1c75-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c75-111">Строка, идентифицирующая поле.</span><span class="sxs-lookup"><span data-stu-id="f1c75-111">A string that identifies the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1c75-112"><strong>Значение</strong></span><span class="sxs-lookup"><span data-stu-id="f1c75-112"><strong>Value</strong></span></span></p></td>
<td><p><span data-ttu-id="f1c75-113">Выражение, которое задает значение, задаваемое в поле.</span><span class="sxs-lookup"><span data-stu-id="f1c75-113">An expression that specifies the value to assign to the field.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f1c75-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f1c75-114">Remarks</span></span>

<span data-ttu-id="f1c75-115">Действие **SetField** не может использоваться вне блока данных **[СоздатьЗапись](createrecord-data-block.md)** или **[ИзменитьЗапись](editrecord-data-block.md)** .</span><span class="sxs-lookup"><span data-stu-id="f1c75-115">The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.</span></span>

