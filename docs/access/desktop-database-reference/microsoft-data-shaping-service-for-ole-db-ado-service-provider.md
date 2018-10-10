---
title: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a72dcc754f39144da4476c9262b93b920fbfbdf6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481666"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="d6061-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span><span class="sxs-lookup"><span data-stu-id="d6061-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="d6061-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6061-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d6061-104">Служба формирования данных Microsoft для поставщика OLE DB служба поддерживает построение объектов иерархических (формы) [набора записей](recordset-object-ado.md) из поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="d6061-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="d6061-105">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="d6061-105">Provider Keyword</span></span>

<span data-ttu-id="d6061-106">Для запуска службы формирования данных для OLE DB, укажите следующие ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d6061-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="d6061-107">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="d6061-107">Dynamic Properties</span></span>

<span data-ttu-id="d6061-108">При вызове этого поставщика услуг в семейство сайтов [Свойства](properties-collection-ado.md) объект [подключения](connection-object-ado.md) добавляются следующие динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="d6061-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6061-109">Имя динамического свойства</span><span class="sxs-lookup"><span data-stu-id="d6061-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="d6061-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d6061-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6061-111"><strong>Изменения формы уникальные имена</strong></span><span class="sxs-lookup"><span data-stu-id="d6061-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="d6061-112">Указывает, разрешены ли объекты <strong>набора записей</strong> с повторяющихся значений для их <strong>Изменить имя</strong> свойства.</span><span class="sxs-lookup"><span data-stu-id="d6061-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="d6061-113">Если это динамических свойство имеет <strong>значение True,</strong> и создается новый <strong>набор записей</strong> изменить имя же определенные пользователем форму как существующих <strong>записей</strong>, а затем изменяется имя нового объекта <strong>набора записей</strong> изменения формы, чтобы сделать его уникальным.</span><span class="sxs-lookup"><span data-stu-id="d6061-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="d6061-114">Если это свойство имеет <strong>значение False</strong> и создания нового <strong>набора записей</strong> с изменить имя же определенные пользователем форму как существующих <strong>записей</strong>, оба <strong>набора записей</strong> объекта будет иметь такой же изменить имя.</span><span class="sxs-lookup"><span data-stu-id="d6061-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="d6061-115">Таким образом ни один из <strong>набора записей</strong> форму можно изменить до тех пор, пока существует оба набора записей.</span><span class="sxs-lookup"><span data-stu-id="d6061-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="d6061-116">Значение по умолчанию свойства имеет <strong>значение False</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6061-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6061-117"><strong>Поставщик данных</strong></span><span class="sxs-lookup"><span data-stu-id="d6061-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d6061-118">Указывает имя поставщика, который будет предоставлять строки, чтобы иметь форму.</span><span class="sxs-lookup"><span data-stu-id="d6061-118">Indicates the name of the provider that will supply rows to be shaped.</span></span> <span data-ttu-id="d6061-119">Это значение может быть нет, если поставщик не будет использоваться для предоставления строк.</span><span class="sxs-lookup"><span data-stu-id="d6061-119">This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6061-120">Можно также установить для записи динамические свойства путем указания их имена в качестве ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="d6061-120">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="d6061-121">Например в Microsoft Visual Basic, задайте для свойства динамических **Поставщика данных** для «MSDASQL», указав:</span><span class="sxs-lookup"><span data-stu-id="d6061-121">For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="d6061-122">Можно также задать или получить динамического свойства, указав его имя в качестве индекса в [поле свойства](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d6061-122">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property.</span></span> <span data-ttu-id="d6061-123">К примеру получить и печать текущее значение свойства динамической **Поставщика данных** , а затем задать новое значение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6061-123">For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="d6061-124">Дополнительные сведения о данных формирования [Формирования данных](data-shaping-summary.md)см.</span><span class="sxs-lookup"><span data-stu-id="d6061-124">For more information about data shaping, see [Data Shaping](data-shaping-summary.md).</span></span>

