---
title: Метод Cancel (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e80763ddad86a63aec605371b58ffeab383681dd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944020"
---
# <a name="cancel-method-ado"></a><span data-ttu-id="f7c9c-102">Метод Cancel (ADO)</span><span class="sxs-lookup"><span data-stu-id="f7c9c-102">Cancel method (ADO)</span></span>

<span data-ttu-id="f7c9c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7c9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7c9c-104">Отменяет выполнение ожидающих асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="f7c9c-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c9c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7c9c-105">Syntax</span></span>

<span data-ttu-id="f7c9c-106">*объект*. Отмена</span><span class="sxs-lookup"><span data-stu-id="f7c9c-106">*object*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c9c-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7c9c-107">Remarks</span></span>

<span data-ttu-id="f7c9c-108">Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода (то есть, метод, вызываемый с параметром **adAsyncConnect**, **adAsyncExecute**или **adAsyncFetch** ).</span><span class="sxs-lookup"><span data-stu-id="f7c9c-108">Use the **Cancel** method to terminate execution of an asynchronous method call (that is, a method invoked with the **adAsyncConnect**, **adAsyncExecute**, or **adAsyncFetch** option).</span></span>

<span data-ttu-id="f7c9c-109">В следующей таблице показаны какие задачи останавливается при использовании метода **Cancel** на определенный тип объекта.</span><span class="sxs-lookup"><span data-stu-id="f7c9c-109">The following table shows what task is terminated when you use the **Cancel** method on a particular type of object.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<span data-ttu-id="f7c9c-110">Если <em>объект</em> является</span><span class="sxs-lookup"><span data-stu-id="f7c9c-110">If <em>object</em> is a</span></span></p></th>
<th><p><span data-ttu-id="f7c9c-111">Последний асинхронного вызова этого метода будет завершен</span><span class="sxs-lookup"><span data-stu-id="f7c9c-111">The last asynchronous call to this method is terminated</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7c9c-112"><a href="command-object-ado.md">Команда</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-112"><a href="command-object-ado.md">Command</a></span></span></p></td>
<td><p><span data-ttu-id="f7c9c-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Выполнение</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-113"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7c9c-114"><a href="connection-object-ado.md">Подключение</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-114"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="f7c9c-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Выполнение</a> или <a href="open-method-ado-connection.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-115"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</a> or <a href="open-method-ado-connection.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7c9c-116"><a href="record-object-ado.md">Запись</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-116"><a href="record-object-ado.md">Record</a></span></span></p></td>
<td><p><span data-ttu-id="f7c9c-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">макрокоманду УдалитьЗапись</a>, <a href="moverecord-method-ado.md">MoveRecord</a>или <a href="open-method-ado-record.md">Открыть</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-117"><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">DeleteRecord</a>, <a href="moverecord-method-ado.md">MoveRecord</a>, or <a href="open-method-ado-record.md">Open</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7c9c-118"><a href="recordset-object-ado.md">Набор записей</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-118"><a href="recordset-object-ado.md">Recordset</a></span></span></p></td>
<td><p><span data-ttu-id="f7c9c-119"><a href="open-method-ado-recordset.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-119"><a href="open-method-ado-recordset.md">Open</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7c9c-120"><a href="stream-object-ado.md">Stream</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-120"><a href="stream-object-ado.md">Stream</a></span></span></p></td>
<td><p><span data-ttu-id="f7c9c-121"><a href="open-method-ado-stream.md">Открытие</a></span><span class="sxs-lookup"><span data-stu-id="f7c9c-121"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
</tr>
</tbody>
</table>

