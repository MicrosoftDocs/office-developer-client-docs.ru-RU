---
title: Visual C++ (Справочник по базам данных Access на компьютере)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 082790c33840bfeacf0c1a6bd38af34c0617f4fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303404"
---
# <a name="visual-c"></a><span data-ttu-id="c2f59-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="c2f59-102">Visual C++</span></span>


<span data-ttu-id="c2f59-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2f59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2f59-104">Это схематическое описание процесса создания экземпляров событий ADO в Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c2f59-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="c2f59-105">Полное описание приведено в статье [Пример модели событий ADO (VC + +)](ado-events-model-example-vc.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f59-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="c2f59-106">Создайте классы, производные от интерфейсов **коннектионевентсвт** и **рекордсетевентсвт** , обнаруженных в файле адоинт. h.</span><span class="sxs-lookup"><span data-stu-id="c2f59-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="c2f59-107">Реализуйте каждый из методов обработчиков событий в обоих классах.</span><span class="sxs-lookup"><span data-stu-id="c2f59-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="c2f59-108">В каждом методе достаточно возвращать значение HRESULT элемента S\_ОК.</span><span class="sxs-lookup"><span data-stu-id="c2f59-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="c2f59-109">Тем не менее, если вы сделаете так, чтобы обработчики событий были доступны, они будут вызываться непрерывно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2f59-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="c2f59-110">Вместо этого можно запрашивать больше уведомлений после первого момента, установив для параметра **адстатус** значение **адстатусунвантедевент**.</span><span class="sxs-lookup"><span data-stu-id="c2f59-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="c2f59-111">Классы событий наследуют от **IUnknown**, поэтому необходимо также реализовать методы **QueryInterface**, **AddRef**и **Release** .</span><span class="sxs-lookup"><span data-stu-id="c2f59-111">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods.</span></span> <span data-ttu-id="c2f59-112">Кроме того, реализуйте конструкторы и деструкторы классов.</span><span class="sxs-lookup"><span data-stu-id="c2f59-112">Also implement class constructors and destructors.</span></span> <span data-ttu-id="c2f59-113">Выберите инструменты Visual C++, с которыми вы наиболее удобно упростить эту часть задачи.</span><span class="sxs-lookup"><span data-stu-id="c2f59-113">Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="c2f59-114">Убедитесь, что обработчики событий доступны, вызвав **QueryInterface** в объекте [Recordset](recordset-object-ado.md) и объектах [подключения](connection-object-ado.md) для интерфейсов **иконнектионпоинтконтаинер** и **IConnectionPoint** .</span><span class="sxs-lookup"><span data-stu-id="c2f59-114">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="c2f59-115">Затем выполните команду **IConnectionPoint:: Advise** для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="c2f59-115">Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="c2f59-116">Например, предположим, что вы используете логическую функцию, которая возвращает **значение true** , если она успешно информирует объект **Recordset** , доступные обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="c2f59-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="c2f59-117">На этом шаге события для семейства **рекордсетевент** включены, и методы будут вызываться как события **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c2f59-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="c2f59-118">В дальнейшем, когда необходимо сделать обработчики событий недоступными, снова получите точку подключения и отправьте метод **IConnectionPoint:: unadvise** .</span><span class="sxs-lookup"><span data-stu-id="c2f59-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="c2f59-119">При необходимости необходимо освобождать интерфейсы и удалять объекты класса.</span><span class="sxs-lookup"><span data-stu-id="c2f59-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="c2f59-120">В приведенном ниже коде показан полный пример класса приемника событий **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c2f59-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

