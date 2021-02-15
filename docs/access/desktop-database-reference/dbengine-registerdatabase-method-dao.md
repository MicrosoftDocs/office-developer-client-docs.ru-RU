---
title: Метод DBEngine.RegisterDatabase (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294227"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="49b61-102">Метод DBEngine.RegisterDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="49b61-102">DBEngine.RegisterDatabase method (DAO)</span></span>

<span data-ttu-id="49b61-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49b61-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49b61-104">Введите сведения о под соединении для источника данных ODBC в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="49b61-104">Enters connection information for an ODBC data source in the Windows Registry.</span></span> <span data-ttu-id="49b61-105">Драйверу ODBC необходимы сведения о под подключениех при открытом источнике данных ODBC во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="49b61-105">The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b61-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49b61-106">Syntax</span></span>

<span data-ttu-id="49b61-107">*выражение .* RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span><span class="sxs-lookup"><span data-stu-id="49b61-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="49b61-108">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="49b61-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="49b61-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49b61-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49b61-110">Имя</span><span class="sxs-lookup"><span data-stu-id="49b61-110">Name</span></span></p></th>
<th><p><span data-ttu-id="49b61-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="49b61-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="49b61-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="49b61-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="49b61-113">Описание</span><span class="sxs-lookup"><span data-stu-id="49b61-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49b61-114"><em>Dsn</em></span><span class="sxs-lookup"><span data-stu-id="49b61-114"><em>Dsn</em></span></span></p></td>
<td><p><span data-ttu-id="49b61-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="49b61-115">Required</span></span></p></td>
<td><p><span data-ttu-id="49b61-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="49b61-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="49b61-117">имя, используемого в <strong><a href="dbengine-opendatabase-method-dao.md">методе OpenDatabase.</a></strong></span><span class="sxs-lookup"><span data-stu-id="49b61-117">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method.</span></span> <span data-ttu-id="49b61-118">Он ссылается на блок описательных сведений об источнике данных.</span><span class="sxs-lookup"><span data-stu-id="49b61-118">It refers to a block of descriptive information about the data source.</span></span> <span data-ttu-id="49b61-119">Например, если источником данных является удаленная база данных ODBC, это может быть имя сервера.</span><span class="sxs-lookup"><span data-stu-id="49b61-119">For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49b61-120"><em>Driver</em></span><span class="sxs-lookup"><span data-stu-id="49b61-120"><em>Driver</em></span></span></p></td>
<td><p><span data-ttu-id="49b61-121">Обязательно</span><span class="sxs-lookup"><span data-stu-id="49b61-121">Required</span></span></p></td>
<td><p><span data-ttu-id="49b61-122"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="49b61-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="49b61-123">Имя драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="49b61-123">The name of the ODBC driver.</span></span> <span data-ttu-id="49b61-124">Это не имя DLL-файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="49b61-124">This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49b61-125"><em>Silent</em></span><span class="sxs-lookup"><span data-stu-id="49b61-125"><em>Silent</em></span></span></p></td>
<td><p><span data-ttu-id="49b61-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="49b61-126">Required</span></span></p></td>
<td><p><span data-ttu-id="49b61-127"><strong>Логический</strong></span><span class="sxs-lookup"><span data-stu-id="49b61-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="49b61-128"><strong>True,</strong> если вы не хотите отображать диалоговое окно драйвера ODBC с запросом сведений о драйверах; Или <strong>false,</strong> если вы хотите отобразить диалоговое окно драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="49b61-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="49b61-129">Если параметр silent имеет <strong>true,</strong>атрибуты должны содержать все необходимые сведения, необходимые для драйверов, иначе диалоговое окно все равно будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="49b61-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49b61-130"><em>Атрибуты</em></span><span class="sxs-lookup"><span data-stu-id="49b61-130"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="49b61-131">Обязательно</span><span class="sxs-lookup"><span data-stu-id="49b61-131">Required</span></span></p></td>
<td><p><span data-ttu-id="49b61-132"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="49b61-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="49b61-133">Список ключевых слов, добавляемого в реестр Windows.</span><span class="sxs-lookup"><span data-stu-id="49b61-133">A list of keywords to be added to the Windows Registry.</span></span> <span data-ttu-id="49b61-134">Ключевые слова находятся в строке с делегировкой возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="49b61-134">The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="49b61-135">Заметки</span><span class="sxs-lookup"><span data-stu-id="49b61-135">Remarks</span></span>

<span data-ttu-id="49b61-136">Если база данных уже зарегистрирована (сведения о под подключениех уже введены) в реестре Windows при использовании метода **RegisterDatabase,** сведения о под подключением обновляются.</span><span class="sxs-lookup"><span data-stu-id="49b61-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="49b61-137">Если метод **RegisterDatabase** по какой-либо причине не удается, в реестр Windows не внося никаких изменений и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="49b61-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="49b61-138">Дополнительные сведения о драйверах ODBC, таких как SQL Server, см. в файле справки, предоставленного драйвером.</span><span class="sxs-lookup"><span data-stu-id="49b61-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="49b61-139">Пример</span><span class="sxs-lookup"><span data-stu-id="49b61-139">Example</span></span>

<span data-ttu-id="49b61-140">В этом примере метод **RegisterDatabase** используется для регистрации Microsoft SQL Server данных Publishers в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="49b61-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

