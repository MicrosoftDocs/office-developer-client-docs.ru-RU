---
title: Метод Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e740d04b27b0154cd3621d870590cb522c2a239e
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026437"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="69891-102">Метод Refresh (RDS)</span><span class="sxs-lookup"><span data-stu-id="69891-102">Refresh method (RDS)</span></span>

<span data-ttu-id="69891-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69891-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69891-104">Повторный запрос источника данных, указанных в свойстве [подключение](connect-property-rds.md) и обновляет результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="69891-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="69891-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69891-105">Syntax</span></span>

<span data-ttu-id="69891-106">*DataControl*. Обновление</span><span class="sxs-lookup"><span data-stu-id="69891-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="69891-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="69891-107">Parameters</span></span>

|<span data-ttu-id="69891-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="69891-108">Parameter</span></span>|<span data-ttu-id="69891-109">Описание</span><span class="sxs-lookup"><span data-stu-id="69891-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="69891-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="69891-110">*DataControl*</span></span> |<span data-ttu-id="69891-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="69891-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="69891-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="69891-112">Remarks</span></span>

<span data-ttu-id="69891-113">Прежде чем использовать метод **Refresh** , необходимо задать свойства [подключения](connect-property-rds.md), [сервер](server-property-rds.md)и [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) .</span><span class="sxs-lookup"><span data-stu-id="69891-113">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) properties before you use the **Refresh** method.</span></span> <span data-ttu-id="69891-114">Все элементы управления с привязкой к данным на форму, связанную с **RDS. DataControl** объекта будет содержать новый набор записей.</span><span class="sxs-lookup"><span data-stu-id="69891-114">All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records.</span></span> <span data-ttu-id="69891-115">Выпущен любого существующего объекта [набора записей](recordset-object-ado.md) и не учитываются несохраненные изменения.</span><span class="sxs-lookup"><span data-stu-id="69891-115">Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded.</span></span> <span data-ttu-id="69891-116">Метод **Refresh** автоматически преобразует первую запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="69891-116">The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="69891-117">Рекомендуется вызвать метод **Refresh** периодически при работе с данными.</span><span class="sxs-lookup"><span data-stu-id="69891-117">It's a good idea to call the **Refresh** method periodically when you work with data.</span></span> <span data-ttu-id="69891-118">Если извлечения данных и оставьте его на клиентском компьютере какое-то время, скорее всего, устаревший.</span><span class="sxs-lookup"><span data-stu-id="69891-118">If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date.</span></span> <span data-ttu-id="69891-119">Существует возможность, что все изменения, внесенные завершится с ошибкой, так как другому пользователю, могут измениться эту запись и отправил изменения перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="69891-119">It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

