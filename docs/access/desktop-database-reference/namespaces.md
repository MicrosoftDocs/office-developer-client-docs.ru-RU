---
title: Пространства имен (Справочник по для настольных баз данных Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc7c0cf302c0b8a297310dfa439ac87724331569
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481923"
---
# <a name="namespaces"></a><span data-ttu-id="6d66d-102">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d66d-102">Namespaces</span></span>


<span data-ttu-id="6d66d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d66d-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="namespaces"></a><span data-ttu-id="6d66d-104">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d66d-104">Namespaces</span></span>

<span data-ttu-id="6d66d-105">Формат сохранения XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6d66d-105">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d66d-106">Префикс</span><span class="sxs-lookup"><span data-stu-id="6d66d-106">Prefix</span></span></p></th>
<th><p><span data-ttu-id="6d66d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6d66d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d66d-108">s</span><span class="sxs-lookup"><span data-stu-id="6d66d-108">s</span></span></p></td>
<td><p><span data-ttu-id="6d66d-109">Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d66d-109">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d66d-110">dt</span><span class="sxs-lookup"><span data-stu-id="6d66d-110">dt</span></span></p></td>
<td><p><span data-ttu-id="6d66d-111">Относится к спецификации определения типа данных.</span><span class="sxs-lookup"><span data-stu-id="6d66d-111">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d66d-112">RS</span><span class="sxs-lookup"><span data-stu-id="6d66d-112">rs</span></span></p></td>
<td><p><span data-ttu-id="6d66d-113">Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6d66d-113">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d66d-114">z</span><span class="sxs-lookup"><span data-stu-id="6d66d-114">z</span></span></p></td>
<td><p><span data-ttu-id="6d66d-115">Относится к схеме текущий набор строк.</span><span class="sxs-lookup"><span data-stu-id="6d66d-115">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6d66d-116">Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации.</span><span class="sxs-lookup"><span data-stu-id="6d66d-116">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="6d66d-117">Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.»</span><span class="sxs-lookup"><span data-stu-id="6d66d-117">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="6d66d-118">Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.</span><span class="sxs-lookup"><span data-stu-id="6d66d-118">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d66d-119">Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».</span><span class="sxs-lookup"><span data-stu-id="6d66d-119">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="6d66d-120">Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.</span><span class="sxs-lookup"><span data-stu-id="6d66d-120">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="6d66d-121">Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ.</span><span class="sxs-lookup"><span data-stu-id="6d66d-121">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="6d66d-122">ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="6d66d-122">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

## <a name="namespaces"></a><span data-ttu-id="6d66d-123">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="6d66d-123">Namespaces</span></span>

<span data-ttu-id="6d66d-124">Формат сохранения XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6d66d-124">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d66d-125">Префикс</span><span class="sxs-lookup"><span data-stu-id="6d66d-125">Prefix</span></span></p></th>
<th><p><span data-ttu-id="6d66d-126">Описание</span><span class="sxs-lookup"><span data-stu-id="6d66d-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d66d-127">s</span><span class="sxs-lookup"><span data-stu-id="6d66d-127">s</span></span></p></td>
<td><p><span data-ttu-id="6d66d-128">Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="6d66d-128">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d66d-129">dt</span><span class="sxs-lookup"><span data-stu-id="6d66d-129">dt</span></span></p></td>
<td><p><span data-ttu-id="6d66d-130">Относится к спецификации определения типа данных.</span><span class="sxs-lookup"><span data-stu-id="6d66d-130">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d66d-131">RS</span><span class="sxs-lookup"><span data-stu-id="6d66d-131">rs</span></span></p></td>
<td><p><span data-ttu-id="6d66d-132">Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6d66d-132">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d66d-133">z</span><span class="sxs-lookup"><span data-stu-id="6d66d-133">z</span></span></p></td>
<td><p><span data-ttu-id="6d66d-134">Относится к схеме текущий набор строк.</span><span class="sxs-lookup"><span data-stu-id="6d66d-134">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6d66d-135">Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации.</span><span class="sxs-lookup"><span data-stu-id="6d66d-135">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="6d66d-136">Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.»</span><span class="sxs-lookup"><span data-stu-id="6d66d-136">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="6d66d-137">Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.</span><span class="sxs-lookup"><span data-stu-id="6d66d-137">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d66d-138">Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».</span><span class="sxs-lookup"><span data-stu-id="6d66d-138">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="6d66d-139">Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.</span><span class="sxs-lookup"><span data-stu-id="6d66d-139">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="6d66d-140">Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ.</span><span class="sxs-lookup"><span data-stu-id="6d66d-140">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="6d66d-141">ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="6d66d-141">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

