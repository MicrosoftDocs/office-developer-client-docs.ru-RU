---
title: Свойство DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 410f11af8daf3912dca9dc78a1cb9216ff8f8dd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294494"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="404ea-102">Свойство DataMember (ADO)</span><span class="sxs-lookup"><span data-stu-id="404ea-102">DataMember property (ADO)</span></span>

<span data-ttu-id="404ea-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="404ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="404ea-104">Указывает имя участника данных, который будет извлечен из объекта, на который ссылается свойство [DataSource.](datasource-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="404ea-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="404ea-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="404ea-105">Settings and return values</span></span>

<span data-ttu-id="404ea-106">Задает или возвращает значение **String.**</span><span class="sxs-lookup"><span data-stu-id="404ea-106">Sets or returns a **String** value.</span></span> <span data-ttu-id="404ea-107">Имя не является конфиденциальным.</span><span class="sxs-lookup"><span data-stu-id="404ea-107">The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="404ea-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="404ea-108">Remarks</span></span>

<span data-ttu-id="404ea-109">Это свойство используется для создания элементов управления, связанных с данными, с помощью среды данных.</span><span class="sxs-lookup"><span data-stu-id="404ea-109">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="404ea-110">Среда данных поддерживает коллекции данных (источников данных), содержащих именуемые объекты *(участники* данных), которые будут представлены в качестве объекта [Recordset.](recordset-object-ado.md) </span><span class="sxs-lookup"><span data-stu-id="404ea-110">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="404ea-111">Свойства **DataMember** и **DataSource** должны использоваться совместно.</span><span class="sxs-lookup"><span data-stu-id="404ea-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="404ea-112">Свойство **DataMember** определяет, какой объект, указанный **свойством DataSource,** будет представлен в качестве объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="404ea-112">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object.</span></span> <span data-ttu-id="404ea-113">Объект **Recordset** должен быть закрыт до заданной цели.</span><span class="sxs-lookup"><span data-stu-id="404ea-113">The **Recordset** object must be closed before this property is set.</span></span> <span data-ttu-id="404ea-114">Ошибка создается, если свойство **DataMember** не задано перед свойством **DataSource** или если имя **DataMember** не распознается объектом, указанным в свойстве **DataSource.**</span><span class="sxs-lookup"><span data-stu-id="404ea-114">An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="404ea-115">**Использование**</span><span class="sxs-lookup"><span data-stu-id="404ea-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
