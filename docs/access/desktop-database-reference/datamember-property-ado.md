---
title: DataMember Property (ADO)
TOCTitle: DataMember Property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a67864ab135c59f146a27f997d4b0df63865a50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483156"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="a352a-102">DataMember Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="a352a-102">DataMember Property (ADO)</span></span>

<span data-ttu-id="a352a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a352a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a352a-104">Указывает имя элемента данных, который извлекается из объекта ссылается свойство [DataSource](datasource-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a352a-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a352a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a352a-105">Settings and Return Values</span></span>

<span data-ttu-id="a352a-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="a352a-106">Sets or returns a **String** value.</span></span> <span data-ttu-id="a352a-107">Имя не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="a352a-107">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="a352a-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="a352a-108">Remarks</span></span>

<span data-ttu-id="a352a-109">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="a352a-109">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="a352a-110">Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект [набора записей](recordset-object-ado.md) *.*</span><span class="sxs-lookup"><span data-stu-id="a352a-110">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="a352a-111">Свойства **DataSource** и **DataMember** должен использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="a352a-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="a352a-112">Свойство **DataMember** определяет, какие объекта, заданного в свойстве **DataSource** будут представлены как объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a352a-112">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object.</span></span> <span data-ttu-id="a352a-113">Объект **набора записей** должны быть закрыты, это свойство задано.</span><span class="sxs-lookup"><span data-stu-id="a352a-113">The **Recordset** object must be closed before this property is set.</span></span> <span data-ttu-id="a352a-114">Ошибка создается в том случае, если свойство **DataMember** не будет установлено перед свойства **источника данных** или имя **DataMember** не распознается объектом, указанных в свойстве **DataSource** .</span><span class="sxs-lookup"><span data-stu-id="a352a-114">An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="a352a-115">**Использование**</span><span class="sxs-lookup"><span data-stu-id="a352a-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
