---
title: ADO Java Class Wrappers
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa3a4d1d2a917997b9e7ed5407d4f2ce8d1d0361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481915"
---
# <a name="ado-java-class-wrappers"></a><span data-ttu-id="760f7-102">ADO Java Class Wrappers</span><span class="sxs-lookup"><span data-stu-id="760f7-102">ADO Java Class Wrappers</span></span>


<span data-ttu-id="760f7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="760f7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="760f7-104">Этот код объявляет экземпляр оболочки класс ADO [записей](recordset-object-ado.md) и инициализирует его, все в той же строке кода.</span><span class="sxs-lookup"><span data-stu-id="760f7-104">This code declares an instance of the ADO [Recordset](recordset-object-ado.md) class wrapper and initializes it, all on the same line of code.</span></span> <span data-ttu-id="760f7-105">Более того он объявляет переменные для каждого из аргументов в метод [Open](open-method-ado-recordset.md) особенно для [LockType для](locktype-property-ado.md) и [CursorType](cursortype-property-ado.md) (поскольку Java не поддерживает перечисляемые типы).</span><span class="sxs-lookup"><span data-stu-id="760f7-105">Further, it declares variables for each of the arguments in the [Open](open-method-ado-recordset.md) method, especially for [LockType](locktype-property-ado.md) and [CursorType](cursortype-property-ado.md) (because Java doesn't support enumerated types).</span></span> <span data-ttu-id="760f7-106">Открывает и закрывает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="760f7-106">It opens and closes the **Recordset** object.</span></span> <span data-ttu-id="760f7-107">Установка Rs1 NULL для просто планирует этой переменной нужно освободить при Java выполняет его систематического и временная выпуска неиспользуемых объектов.</span><span class="sxs-lookup"><span data-stu-id="760f7-107">Setting Rs1 to NULL merely schedules that variable to be released when Java performs its systematic and intermittent release of unused objects.</span></span>

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

