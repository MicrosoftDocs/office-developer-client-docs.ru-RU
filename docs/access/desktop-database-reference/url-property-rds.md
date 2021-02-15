---
title: URL Property (RDS - Access desktop database reference)
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
# <a name="url-property-rds"></a><span data-ttu-id="2f9e4-102">Свойство URL (RDS)</span><span class="sxs-lookup"><span data-stu-id="2f9e4-102">URL property (RDS)</span></span>

<span data-ttu-id="2f9e4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f9e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f9e4-104">Указывает строку, которая содержит относительный или абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2f9e4-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="2f9e4-105">Вы можете установить **свойство URL-адреса** во время разработки в теге OBJECT объекта [DataControl](datacontrol-object-rds.md) или во время запуска в коде скрипта.</span><span class="sxs-lookup"><span data-stu-id="2f9e4-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9e4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f9e4-106">Syntax</span></span>

<span data-ttu-id="2f9e4-107">Время разработки: \< PARAM NAME="URL" VALUE="Server"\></span><span class="sxs-lookup"><span data-stu-id="2f9e4-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="2f9e4-108">Время запуска: DataControl.URL="Server"</span><span class="sxs-lookup"><span data-stu-id="2f9e4-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="2f9e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f9e4-109">Parameters</span></span>

|<span data-ttu-id="2f9e4-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="2f9e4-110">Parameter</span></span>|<span data-ttu-id="2f9e4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2f9e4-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2f9e4-112">*Server*</span><span class="sxs-lookup"><span data-stu-id="2f9e4-112">*Server*</span></span> |<span data-ttu-id="2f9e4-113">**Строка,** содержающая допустимый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2f9e4-113">A **String** value that contains a valid URL.</span></span>|
|<span data-ttu-id="2f9e4-114">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="2f9e4-114">*DataControl*</span></span> |<span data-ttu-id="2f9e4-115">Объектная переменная, представляюная **объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="2f9e4-115">An object variable that represents a **DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2f9e4-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="2f9e4-116">Remarks</span></span>

<span data-ttu-id="2f9e4-117">Обычно URL-адрес определяет файл страницы Active Server (ASP), который может создавать и [возвращать набор записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="2f9e4-117">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="2f9e4-118">Таким образом, пользователь может получить **объект Recordset** без вызова объекта [DataFactory](datafactory-object-rdsserver.md) на стороне сервера или запрограммировать пользовательский бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="2f9e4-118">Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="2f9e4-119">Если свойство **URL-адреса** задано, [SubmitChanges](submitchanges-method-rds.md) будет отправлять изменения в расположение, указанное URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="2f9e4-119">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

