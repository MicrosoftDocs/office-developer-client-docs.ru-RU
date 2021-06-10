---
title: Свойство URL (RDS — доступ к настольной базе данных)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313400"
---
# <a name="url-property-rds"></a><span data-ttu-id="b416f-102">Свойство URL(RDS)</span><span class="sxs-lookup"><span data-stu-id="b416f-102">URL property (RDS)</span></span>

<span data-ttu-id="b416f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b416f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b416f-104">Указывает строку, содержаную относительный или абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b416f-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="b416f-105">Свойство **URL-адреса** можно установить во время разработки в теге OBJECT объекта [DataControl](datacontrol-object-rds.md) или во время запуска в коде скриптов.</span><span class="sxs-lookup"><span data-stu-id="b416f-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b416f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b416f-106">Syntax</span></span>

<span data-ttu-id="b416f-107">Время разработки: \< PARAM NAME="URL"VALUE="Server"\></span><span class="sxs-lookup"><span data-stu-id="b416f-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="b416f-108">Время запуска: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="b416f-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="b416f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b416f-109">Parameters</span></span>

|<span data-ttu-id="b416f-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="b416f-110">Parameter</span></span>|<span data-ttu-id="b416f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b416f-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b416f-112">*Server*</span><span class="sxs-lookup"><span data-stu-id="b416f-112">*Server*</span></span> |<span data-ttu-id="b416f-113">Значение **String,** содержа которое содержит допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b416f-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="b416f-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b416f-114">*DataControl*</span></span> |<span data-ttu-id="b416f-115">Переменная объекта, представляют **объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="b416f-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b416f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="b416f-116">Remarks</span></span>

<span data-ttu-id="b416f-117">Как правило, URL-адрес определяет файл Active Server Page (.asp), который может создавать и возвращать [набор записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b416f-117">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="b416f-118">Таким образом, пользователь может получить **Набор записей,** не вызывая серверный объект [DataFactory](datafactory-object-rdsserver.md) или запрограммировать настраиваемый бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="b416f-118">Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="b416f-119">Если свойство **URL-адреса** задано, [SubmitChanges](submitchanges-method-rds.md) будет отправлять изменения в указанное URL-адресом расположение.</span><span class="sxs-lookup"><span data-stu-id="b416f-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

