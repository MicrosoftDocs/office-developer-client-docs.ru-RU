---
title: Пространства имен (Справочник по для настольных баз данных Access)
TOCTitle: Namespaces
ms:assetid: e39f003c-3d16-1fae-48c5-304593c41f2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250158(v=office.15)
ms:contentKeyID: 48548318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef37f04ec6824cedf773cb72751b2364d2b3edf8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876563"
---
# <a name="namespaces"></a><span data-ttu-id="40dbe-102">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="40dbe-102">Namespaces</span></span>


<span data-ttu-id="40dbe-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40dbe-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="namespaces"></a><span data-ttu-id="40dbe-104">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="40dbe-104">Namespaces</span></span>

<span data-ttu-id="40dbe-105">Формат сохранения XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="40dbe-105">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40dbe-106">Префикс</span><span class="sxs-lookup"><span data-stu-id="40dbe-106">Prefix</span></span></p></th>
<th><p><span data-ttu-id="40dbe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="40dbe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40dbe-108">s</span><span class="sxs-lookup"><span data-stu-id="40dbe-108">s</span></span></p></td>
<td><p><span data-ttu-id="40dbe-109">Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="40dbe-109">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40dbe-110">dt</span><span class="sxs-lookup"><span data-stu-id="40dbe-110">dt</span></span></p></td>
<td><p><span data-ttu-id="40dbe-111">Относится к спецификации определения типа данных.</span><span class="sxs-lookup"><span data-stu-id="40dbe-111">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40dbe-112">RS</span><span class="sxs-lookup"><span data-stu-id="40dbe-112">rs</span></span></p></td>
<td><p><span data-ttu-id="40dbe-113">Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="40dbe-113">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40dbe-114">z</span><span class="sxs-lookup"><span data-stu-id="40dbe-114">z</span></span></p></td>
<td><p><span data-ttu-id="40dbe-115">Относится к схеме текущий набор строк.</span><span class="sxs-lookup"><span data-stu-id="40dbe-115">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40dbe-116">Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации.</span><span class="sxs-lookup"><span data-stu-id="40dbe-116">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="40dbe-117">Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.»</span><span class="sxs-lookup"><span data-stu-id="40dbe-117">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="40dbe-118">Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.</span><span class="sxs-lookup"><span data-stu-id="40dbe-118">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="40dbe-119">Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».</span><span class="sxs-lookup"><span data-stu-id="40dbe-119">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="40dbe-120">Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.</span><span class="sxs-lookup"><span data-stu-id="40dbe-120">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="40dbe-121">Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ.</span><span class="sxs-lookup"><span data-stu-id="40dbe-121">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="40dbe-122">ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="40dbe-122">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

## <a name="namespaces"></a><span data-ttu-id="40dbe-123">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="40dbe-123">Namespaces</span></span>

<span data-ttu-id="40dbe-124">Формат сохранения XML в ADO использует следующие четыре пространства имен.</span><span class="sxs-lookup"><span data-stu-id="40dbe-124">The XML persistence format in ADO uses the following four namespaces.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40dbe-125">Префикс</span><span class="sxs-lookup"><span data-stu-id="40dbe-125">Prefix</span></span></p></th>
<th><p><span data-ttu-id="40dbe-126">Описание</span><span class="sxs-lookup"><span data-stu-id="40dbe-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40dbe-127">s</span><span class="sxs-lookup"><span data-stu-id="40dbe-127">s</span></span></p></td>
<td><p><span data-ttu-id="40dbe-128">Относится к &quot;XML-данные&quot; пространства имен, содержащего элементы и атрибуты, которые определяют схемы текущего <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="40dbe-128">Refers to the &quot;XML-Data&quot; namespace containing the elements and attributes that define the schema of the current <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40dbe-129">dt</span><span class="sxs-lookup"><span data-stu-id="40dbe-129">dt</span></span></p></td>
<td><p><span data-ttu-id="40dbe-130">Относится к спецификации определения типа данных.</span><span class="sxs-lookup"><span data-stu-id="40dbe-130">Refers to the data type definitions specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40dbe-131">RS</span><span class="sxs-lookup"><span data-stu-id="40dbe-131">rs</span></span></p></td>
<td><p><span data-ttu-id="40dbe-132">Относится к области имен, содержащие элементы и атрибуты, относящиеся к свойствам ADO <strong>записей</strong> и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="40dbe-132">Refers to the namespace containing elements and attributes specific to ADO <strong>Recordset</strong> properties and attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40dbe-133">z</span><span class="sxs-lookup"><span data-stu-id="40dbe-133">z</span></span></p></td>
<td><p><span data-ttu-id="40dbe-134">Относится к схеме текущий набор строк.</span><span class="sxs-lookup"><span data-stu-id="40dbe-134">Refers to the schema of the current rowset.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40dbe-135">Клиент не следует добавлять собственные теги следующие пространства имен, определенный в спецификации.</span><span class="sxs-lookup"><span data-stu-id="40dbe-135">A client should not add its own tags to these namespaces, as defined by the specification.</span></span> <span data-ttu-id="40dbe-136">Например, клиент не задавайте имен как «urn: schemas-microsoft-com:rowset» и затем записать что-нибудь, например «rs: MyOwnTag.»</span><span class="sxs-lookup"><span data-stu-id="40dbe-136">For example, a client should not define a namespace as "urn:schemas-microsoft-com:rowset" and then write out something such as "rs:MyOwnTag."</span></span> <span data-ttu-id="40dbe-137">Дополнительные сведения о пространствах имен [XML](https://www.w3.org/tr/xml-names/)см.</span><span class="sxs-lookup"><span data-stu-id="40dbe-137">To learn more about namespaces, see [XML Namespaces](https://www.w3.org/tr/xml-names/).</span></span>


> [!NOTE]
> <P><span data-ttu-id="40dbe-138">Идентификатор для тега схемы должен быть «RowsetSchema» и пространство имен, используемое для ссылки на схему текущий набор строк должен указывать «#RowsetSchema».</span><span class="sxs-lookup"><span data-stu-id="40dbe-138">The ID for the schema tag must be "RowsetSchema," and the namespace used to refer to the schema of the current rowset must point to "#RowsetSchema."</span></span></P>



<span data-ttu-id="40dbe-139">Обратите внимание, что префикс пространства имен, в правой части двоеточие и слева от знака равенства, произвольных.</span><span class="sxs-lookup"><span data-stu-id="40dbe-139">Note that the prefix of the namespace, that part to the right of the colon and to the left of the equal sign, is arbitrary.</span></span>

```vb 
 
xmlns:rs="urn:schemas-microsoft-com:rowset" 
```

<span data-ttu-id="40dbe-140">Пользователь может указать это будет любое имя, поскольку это имя будет использоваться постоянно в XML-документ.</span><span class="sxs-lookup"><span data-stu-id="40dbe-140">The user can define this to be any name as long as this name is consistently used throughout the XML document.</span></span> <span data-ttu-id="40dbe-141">ADO всегда считывает «s,» «rs», «dt» и «z», но эти имена префикс не жестко в компонент загрузки.</span><span class="sxs-lookup"><span data-stu-id="40dbe-141">ADO always writes out "s," "rs," "dt," and "z," but these prefix names are not hard-coded into the loading component.</span></span>

