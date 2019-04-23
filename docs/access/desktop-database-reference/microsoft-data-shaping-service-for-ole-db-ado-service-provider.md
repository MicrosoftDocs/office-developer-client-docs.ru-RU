---
title: Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288962"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="03c06-102">Служба формирования данных (Майкрософт) для OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="03c06-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="03c06-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03c06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03c06-104">Служба формирования данных Майкрософт для поставщика службы OLE DB поддерживает создание иерархических объектов [Recordset](recordset-object-ado.md) от поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="03c06-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="03c06-105">Ключевое слово Provider</span><span class="sxs-lookup"><span data-stu-id="03c06-105">Provider Keyword</span></span>

<span data-ttu-id="03c06-106">Чтобы вызвать службу формирования данных для OLE DB, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="03c06-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="03c06-107">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="03c06-107">Dynamic Properties</span></span>

<span data-ttu-id="03c06-108">При вызове этого поставщика услуг следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="03c06-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03c06-109">Имя динамического свойства</span><span class="sxs-lookup"><span data-stu-id="03c06-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="03c06-110">Описание</span><span class="sxs-lookup"><span data-stu-id="03c06-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03c06-111"><strong>Уникальные имена перерисовки</strong></span><span class="sxs-lookup"><span data-stu-id="03c06-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="03c06-112">Указывает, разрешены ли объекты <strong>Recordset</strong> с повторяющимися значениями свойств <strong>имени</strong> перерисовки.</span><span class="sxs-lookup"><span data-stu-id="03c06-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="03c06-113">Если это динамическое свойство имеет <strong>значение true</strong> и создан новый <strong>набор записей</strong> с таким же пользовательским именем изменения фигуры, что и у существующего объекта <strong>Recordset</strong>, то имя нового объекта <strong>Recordset</strong> изменяется, чтобы сделать его уникальным.</span><span class="sxs-lookup"><span data-stu-id="03c06-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="03c06-114">Если это свойство имеет <strong>значение false</strong> и создан новый <strong>набор записей</strong> с тем же именем, что и у существующего объекта Recordset, <strong></strong>то оба объекта <strong>Recordset</strong> будут иметь одно и то же имя изменения формы.</span><span class="sxs-lookup"><span data-stu-id="03c06-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="03c06-115">Поэтому ни один из <strong>наборов записей</strong> не может быть переопределен до тех пор, пока оба объекта Recordset существуют.</span><span class="sxs-lookup"><span data-stu-id="03c06-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="03c06-116">Значение свойства по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="03c06-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03c06-117"><strong>Поставщик данных</strong></span><span class="sxs-lookup"><span data-stu-id="03c06-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="03c06-118">Указывает имя поставщика, который будет предоставлять строки в форме.</span><span class="sxs-lookup"><span data-stu-id="03c06-118">Indicates the name of the provider that will supply rows to be shaped.</span></span> <span data-ttu-id="03c06-119">Это значение может быть равно NONE, если поставщик не будет использоваться для предоставления строк.</span><span class="sxs-lookup"><span data-stu-id="03c06-119">This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03c06-120">Вы также можете задать динамические свойства для записи, указав их имена в виде ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="03c06-120">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="03c06-121">Например, в Microsoft Visual Basic задайте динамическое свойство **Data Provider** равным "мсдаскл", указав следующее:</span><span class="sxs-lookup"><span data-stu-id="03c06-121">For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="03c06-122">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для свойства [Properties](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="03c06-122">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property.</span></span> <span data-ttu-id="03c06-123">Например, получите и распечатайте текущее значение динамического свойства **поставщика данных** , а затем задайте новое значение, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="03c06-123">For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="03c06-124">Дополнительные сведения о процессе формирования данных см. [](data-shaping.md)</span><span class="sxs-lookup"><span data-stu-id="03c06-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

