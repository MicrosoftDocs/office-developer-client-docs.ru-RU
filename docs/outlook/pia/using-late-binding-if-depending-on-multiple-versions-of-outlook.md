---
title: Использование позднего связывания при использовании нескольких версий Outlook
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4cca4d426e5e7e9fd06fa3a0c3af1158b7e6c2f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706900"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>Использование позднего связывания при использовании нескольких версий Outlook

Управляемые надстройки Outlook, использующие основную сборку взаимодействия (PIA) Outlook, компилируются сведениями о типах, которые предоставляет PIA. Это **раннее связывание** сведений о типах для методов и свойств позволяет компилятору выполнять проверки типов и синтаксиса, чтобы гарантировать передачу в метод или свойство правильного количества и правильных типов параметров, а также принадлежность возвращаемого значения к ожидаемому типу. 

Но к недостаткам раннего связывания относится появление несовместимости версий, если для метода или свойства, вызываемых надстройкой, в более ранней версии используется другое объявление. Например, добавление новых методов и свойств или изменение существующих членов объекта может изменить двоичную структуру объекта и вызвать проблемы в управляемой надстройке, использующей более новые сведения для автоматизации ранней версии Outlook. 

В подобных случаях при **позднем связывании** привязка вызовов свойств и методов к объектам выполняется во время выполнения. Позднее связывание помогает избежать сложностей, вызванных типами, отличающимися в различных версиях Outlook, и особенно полезно при написании надстроек, опирающихся на несколько различных версий Outlook.

Позднее связывание включает вызов надстройкой интерфейса [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch), реализованного Outlook. Для использования позднего связывания в Visual C\# применяйте метод [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2). Этот метод вызывает [IDispatch::GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [IDispatch::Invoke](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke), чтобы выполнить связывание с методами и свойствами Outlook. Метод IDispatch::GetIdsOfNames позволяет Visual C\# опрашивать объект о поддерживаемых методах и свойствах, а метод IDispatch::Invoke затем позволяет Visual C\# вызывать эти методы и свойства. 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>См. также

- [Введение во взаимодействие между COM и .NET](introduction-to-interoperability-between-com-and-net.md)

