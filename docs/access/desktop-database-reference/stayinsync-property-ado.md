---
title: Свойство StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703232"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="451f1-102">Свойство StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="451f1-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="451f1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="451f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="451f1-104">Указывает, в объект [набора записей](recordset-object-ado.md) иерархических ли ссылку на базовый дочерние записи (то есть, *главы*) изменяется при изменении позиции строки родительского.</span><span class="sxs-lookup"><span data-stu-id="451f1-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="451f1-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="451f1-105">Settings and return values</span></span>

<span data-ttu-id="451f1-106">Задает или возвращает значение **типа Boolean** .</span><span class="sxs-lookup"><span data-stu-id="451f1-106">Sets or returns a **Boolean** value.</span></span> <span data-ttu-id="451f1-107">Значение по умолчанию — **True**.</span><span class="sxs-lookup"><span data-stu-id="451f1-107">The default value is **True**.</span></span> <span data-ttu-id="451f1-108">Если **значение True**, главы будут обновлены, если изменения объекта **набора записей** родительской строки положение; Если **значение False**, главы будет продолжать ссылаться на данные в предыдущей главе, даже если родительский объект **набора записей** изменилось положение строки.</span><span class="sxs-lookup"><span data-stu-id="451f1-108">If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="451f1-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="451f1-109">Remarks</span></span>

<span data-ttu-id="451f1-110">Это свойство применяется к иерархические наборы записей, такие как те, поддерживаемые [Службой формирования Microsoft данных для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)и должно быть равно на родительский **записей** перед дочерними извлекается **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="451f1-110">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved.</span></span> <span data-ttu-id="451f1-111">Это свойство упрощает переход иерархические наборы записей.</span><span class="sxs-lookup"><span data-stu-id="451f1-111">This property simplifies navigating hierarchical recordsets.</span></span>

