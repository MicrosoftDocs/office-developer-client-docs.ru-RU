---
title: Многочитание и раздор памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- многопотоковые функции excel, раздор памяти в Excel,функции [Excel 2007], функции thread-safe ,thread-safe [Excel 2007],thread-local memory [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301640"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Многочитание и раздор памяти в Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Версии Microsoft Excel до 2007 Excel использовать один поток для всех вычислений таблицы. Однако, начиная Excel 2007 г., Excel можно настроить для использования от 1 до 1024 одновременно потоков для вычисления таблицы. На многопроцессовом или многоядерном компьютере количество потоков по умолчанию равно количеству процессоров или ядер. Поэтому ячейки, безопасные для потоков, или ячейки, содержащие только безопасные нитки, могут быть выделены одновечерным потокам с учетом обычной логики пересчета, которую необходимо вычислить после их прецедентов.
  
## <a name="thread-safe-functions"></a>Thread-Safe Функции

Большинство встроенных функций таблицы, начиная с Excel 2007 г., безопасны для потоков. Вы также можете записывать и регистрировать функции XLL как безопасные потоки. Excel использует один поток (основной поток) для вызова всех команд, функций, небезопасных для потока, **функций xlAutoFree** (за исключением [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12),** а также функций COM и Visual Basic для приложений (VBA).
  
Если функция XLL возвращает XLOPER или **XLOPER12** с набором **xlbitDLLFree,** Excel использует тот же поток, по которому был выполнен вызов функции для вызова **xlAutoFree** или **xlAutoFree12.**  Вызов **xlAutoFree** или **xlAutoFree12** будет выполнен до следующего вызова функции в этом потоке. 
  
Для разработчиков XLL есть преимущества для создания функций, безопасных для потоков:
  
- Они позволяют Excel использовать многопроцесный или многоядерный компьютер.
    
- Они открывают возможность использования удаленных серверов гораздо эффективнее, чем можно сделать с помощью одного потока.
    
Предположим, что у вас есть компьютер с одним процессором, настроенный для использования, скажем, *N-потоков.* Предположим, что запущена таблица, которая выполняет большое количество вызовов для функции XLL, которая, в свою очередь, отправляет запрос на данные или вычисления, которые будут выполняться на удаленный сервер или кластер серверов. В зависимости от топологии дерева зависимостей можно Excel почти одновременно вызывать функцию N times. При условии, что сервер или серверы являются достаточно быстрыми или параллельными, время пересчета электронной таблицы может быть сокращено до 1/N. 
  
Ключевой проблемой при написании функций, безопасных для потоков, является правильная обработка контента для ресурсов. Это обычно означает раздор памяти, и его можно разбить на две проблемы:
  
- Создание известной памяти будет использоваться только этим потоком.
    
- Обеспечение безопасного доступа к общей памяти несколькими потоками.
    
Первое, что нужно знать, это то, какая память в XLL доступна всем потокам, а что доступно только в текущих потоках выполнения.
  
 **Доступ к всем потокам**
  
- Переменные, структуры и экземпляры классов, объявленные вне тела функции.
    
- Статические переменные, объявленные в теле функции.
    
В этих двух случаях память отложена в блоке памяти DLL, созданном для этого экземпляра DLL. Если другой экземпляр приложения загружает DLL, он получает собственную копию этой памяти, чтобы не было раздора для этих ресурсов за пределами этого экземпляра DLL.
  
 **Доступ только к текущему потоку**
  
- Автоматические переменные в коде функции (включая аргументы функции).
    
В этом случае память отложена в стеке для каждого экземпляра вызова функции.
  
> [!NOTE]
> Область динамически выделенной памяти зависит от области указки, указываемой на нее: если указатель доступен всем потокам, память также. Если указатель является автоматической переменной в функции, выделенная память фактически является закрытой для этого потока. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Память, доступная только одним потоком: Thread-Local памяти

Учитывая, что статические переменные в теле функции доступны всем потокам, те функции, которые их используют, явно не являются безопасными для потока. Один экземпляр функции на одном потоке может изменять значение, а другой экземпляр в другом потоке предполагает, что это нечто совершенно другое. 
  
Существует две причины объявления статических переменных в функции:
  
1. Статические данные сохраняются от одного звонка к следующему.
    
2. Указатель на статические данные можно безопасно возвращать функцией.
    
В случае первой причины может потребоваться иметь данные, которые сохраняются и имеют значение для всех вызовов к функции: возможно, простой счетчик, который приращен каждый раз, когда функция вызывается на любом потоке, или структура, которая собирает данные об использовании и производительности на каждом вызове. Вопрос заключается в том, как защитить общие данные или структуру данных. Это лучше всего сделать с помощью критического раздела, как объясняется в следующем разделе.
  
Если данные предназначены только для использования этим потоком, что может быть аргументом 1 и всегда имеется по причине 2, возникает вопрос, как создать память, которая сохраняется, но доступна только из этого потока. Одним из решений является использование API локального хранилища потоков (TLS).
  
Например, рассмотрим функцию, возвращаемую указатель в **XLOPER.**
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Эта функция не является безопасной для потока, так как один поток может возвращать **статический XLOPER12,** а другой переописывание. Вероятность этого еще выше, если **XLOPER12** необходимо передать **xlAutoFree12.** Одним из решений является выделение **XLOPER12,** возвращение указателя к ней и реализация **xlAutoFree12,** чтобы сама **память XLOPER12** была освобождена. Этот подход используется во многих примерах функций, показанных в области управления памятью [в Excel.](memory-management-in-excel.md)
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Этот подход проще реализовать, чем подход, описанный в следующем разделе, который опирается на API TLS, но он имеет некоторые недостатки. Сначала Excel **xlAutoFree** /  **xlAutoFree12** независимо от типа возвращенного  /  **XLOPER XLOPER12.** Во-вторых, при возвращении **XLOPER XLOPER12** s возникает проблема, которая является возвратным значением вызова к функции обратного вызова /  API C. XLOPER XLOPER12 может указать на память, которую необходимо освободить Excel, но сам  /   **XLOPER** /  **XLOPER12** должен быть освобожден таким же образом, как был выделен. Если такой **XLOPER XLOPER12** используется в качестве возвращаемого значения функции таблицы XLL, нет простого способа сообщить /  **xlAutoFree** /  **xlAutoFree12** о необходимости освободить оба указателя соответствующим образом. (Установка **xlbitXLFree** и **xlbitDLLFree** не решает проблему, так как обработка **XLOPER/XLOPER12 в** Excel с обоими наборами неопределена и может измениться с версии на версию.) Чтобы решить эту проблему, XLL может создавать глубокие копии всех выделенных Excel **XLOPER/XLOPER12,** возвращаемого в таблицу. 
  
Решение, которое позволяет избежать этих ограничений, заключается в заполнении и возвращении локального потока **XLOPER/XLOPER12,** который требует, чтобы **xlAutoFree/xlAutoFree12** не освободил сам указатель **XLOPER/XLOPER12.** 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Следующий вопрос заключается в том, как настроить и получить локализованную память потока, другими словами, как реализовать функцию get_thread_local_xloper12 **в** предыдущем примере. Это делается с помощью API локального служба хранилища потока (TLS). Первый шаг — получение индекса TLS с помощью **TlsAlloc,** который в конечном счете должен быть выпущен с **помощью TlsFree.** Оба наиболее наилучшим образом выполняются из **DllMain**.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

После получения индекса следующий шаг — выделение блока памяти для каждого потока. Документация [Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) разработки рекомендует делать это каждый раз, когда функция  **вызова DllMain** вызвана с событием DLL_THREAD_ATTACH, и освободить **память** на каждом DLL_THREAD_DETACH . Однако, следуя этому совету, DLL будет делать ненужные работы для потоков, не используемых для пересчета. 
  
Вместо этого лучше использовать стратегию выделения на первом этапе использования. Сначала необходимо определить структуру, которую необходимо выделить для каждого потока. В предыдущих примерах, возвращая **XLOPERs** или **XLOPER12,** достаточно следующих примеров, но можно создать любую структуру, удовлетворяемую вашим потребностям.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Следующая функция получает указатель локального экземпляра потока или выделяет его, если это первый вызов.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Теперь вы можете увидеть, как получается локализованная память **XLOPER/XLOPER12:** сначала вы получаете указатель экземпляра потока **TLS_data,** а затем возвращаете указатель на **XLOPER/XLOPER12,** содержащийся в нем, как по этому. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Функции **mtr_safe_example_1** **и mtr_safe_example_2** могут быть зарегистрированы в качестве функций таблицы, безопасной для потоков, при Excel. Однако нельзя смешивать два подхода в одном XLL. XLL может экспортировать только одну реализацию **xlAutoFree** и **xlAutoFree12,** и для каждой стратегии памяти требуется другой подход. С **mtr_safe_example_1** указатель, переданный **xlAutoFree/xlAutoFree12,** должен быть освобожден вместе с любыми данными, на которые он указывает. С **mtr_safe_example_2** необходимо освободить только заостряные данные.
  
Windows также предоставляет функцию **GetCurrentThreadId,** которая возвращает уникальный системный ID текущего потока. Это предоставляет разработчику другой способ сделать поток кода безопасным или сделать его поток поведения конкретным.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Память, доступная только к более чем одному потоку: критически важные разделы

Необходимо защитить память чтения и записи, к ней можно получить доступ с помощью более чем одного потока с помощью критически важных разделов. Для каждого блока памяти, который необходимо защитить, необходим критический раздел с именем. Вы можете инициализировать их во время вызова функции **xlAutoOpen** и освободить их и установить их на нуль во время вызова функции **xlAutoClose.** Затем необходимо содержать каждый доступ к защищенной блокировке в паре звонков **в EnterCriticalSection** и **LeaveCriticalSection.** В критический раздел разрешен только один поток в любое время. Вот пример инициализации, унининиализации и использования раздела **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Другой, возможно, более безопасный способ защиты блока памяти —  создать класс, содержащий собственные CRITICAL_SECTION и методы конструктора, деструктора и вспомогательного оборудования. Этот подход имеет дополнительное преимущество защиты объектов, которые могут быть инициализированы до запуска **xlAutoOpen,** или выживания после того, как **называется xlAutoClose,** но следует быть осторожными при создании слишком многих критических разделов и накладных расходов операционной системы, которые это создаст. 
  
Если у вас есть код, который требует одновременного доступа к более чем одному блоку защищенной памяти, необходимо очень внимательно рассмотреть порядок, в котором вписались и выходят критически важные разделы. Например, следующие две функции могут создать тупик.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Если первая функция на одном потоке **g_csSharedTableA,** а вторая на другом потоке вступает **g_csSharedTableB,** оба потока висят. Правильный подход заключается в том, чтобы ввести в последовательном порядке и выйти в обратном порядке, как следует.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Там, где это возможно, лучше с точки зрения сотрудничества потоков изолировать доступ к отдельным блокам, как показано здесь.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Если существует много спорных моментов для общего ресурса, например частые запросы на кратковременный доступ, следует рассмотреть возможность вращения критического раздела. Это метод, который делает ожидание ресурса менее интенсивной обработкой. Для этого можно использовать **initializeCriticalSectionAndSpinCount** при инициализации раздела или **SetCriticalSectionSpinCount** после инициализации, чтобы установить количество циклов потоков до ожидания, когда будут доступны ресурсы. Операция ожидания является дорогостоящей, поэтому вращающийся позволяет избежать этого, если ресурс будет освобожден в то же время. В одной системе процессора количество спинов фактически игнорируется, но вы все равно можете указать его, не причинив вреда. Диспетчер кучи памяти использует количество спина в 4000. Дополнительные сведения об использовании критически важных разделов см. в Windows документации SDK. 
  
## <a name="see-also"></a>См. также



[Управление памятью в Excel](memory-management-in-excel.md)
  
[Многопоточный пересчет в Excel](multithreaded-recalculation-in-excel.md)
  
[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

