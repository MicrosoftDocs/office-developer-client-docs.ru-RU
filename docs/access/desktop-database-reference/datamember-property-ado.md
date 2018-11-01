---
title: Свойство DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eebd4e485c358ed141e6bcb5dc84c82d41fd88ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870151"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="00c78-102">Свойство DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="00c78-102">DataMember property (ADO)</span></span>

<span data-ttu-id="00c78-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00c78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00c78-104">Указывает имя элемента данных, который извлекается из объекта ссылается свойство [DataSource](datasource-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="00c78-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="00c78-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="00c78-105">Settings and return values</span></span>

<span data-ttu-id="00c78-106">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="00c78-106">Sets or returns a **String** value.</span></span> <span data-ttu-id="00c78-107">Имя не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="00c78-107">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c78-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="00c78-108">Remarks</span></span>

<span data-ttu-id="00c78-109">Это свойство используется для создания элементов управления с привязкой к данным с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="00c78-109">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="00c78-110">Среда данных поддерживает коллекций данных (источники данных), содержащий с именем объекты (*элементы данных*), которые будут представлены как объект [набора записей](recordset-object-ado.md) *.*</span><span class="sxs-lookup"><span data-stu-id="00c78-110">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="00c78-111">Свойства **DataSource** и **DataMember** должен использоваться вместе.</span><span class="sxs-lookup"><span data-stu-id="00c78-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="00c78-112">Свойство **DataMember** определяет, какие объекта, заданного в свойстве **DataSource** будут представлены как объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="00c78-112">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object.</span></span> <span data-ttu-id="00c78-113">Объект **набора записей** должны быть закрыты, это свойство задано.</span><span class="sxs-lookup"><span data-stu-id="00c78-113">The **Recordset** object must be closed before this property is set.</span></span> <span data-ttu-id="00c78-114">Ошибка создается в том случае, если свойство **DataMember** не будет установлено перед свойства **источника данных** или имя **DataMember** не распознается объектом, указанных в свойстве **DataSource** .</span><span class="sxs-lookup"><span data-stu-id="00c78-114">An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="00c78-115">**Использование**</span><span class="sxs-lookup"><span data-stu-id="00c78-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
