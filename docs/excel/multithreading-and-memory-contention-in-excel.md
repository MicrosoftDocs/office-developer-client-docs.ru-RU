---
title: Многопоточность и конфликты памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Многопоточность в excel, конфликтов памяти в Excel, функции [Excel 2007], являющихся потокобезопасными, являющихся потокобезопасными функции памяти локального потока [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807317"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Многопоточность и конфликты памяти в Excel

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Чем Excel 2007 версиям Microsoft Excel использовать единый поток для всех расчетов на листе. Тем не менее начиная с версии Excel 2007, Excel может быть настроена на использование от 1 для 1024 параллельных потоков для расчета рабочего листа. Компьютера с несколькими процессорами или многоядерная по умолчанию количество потоков равно числу процессоров или ядер. Таким образом являющихся потокобезопасными ячеек или ячеек, которые содержат только функции, которые являются потокобезопасными, может быть предоставлена параллельных потоков, может быть обычным пересчета логику для вычисления после их влияющие ячейки.
  
## <a name="thread-safe-functions"></a>Функции потоками

Большая часть встроенных функций, начиная с версии Excel 2007 являются потокобезопасными. Также можно записать и зарегистрировать функции XLL как потокобезопасными. Excel использует один поток (главный поток) для вызова всех команд, поток небезопасных функций, функций **xlAuto** (за исключением [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12**) и COM и Visual Basic для приложений (VBA) функций.
  
В функции XLL возвращает **XLOPER** или **XLOPER12** с набором **xlbitDLLFree** , Excel использует тот же поток, на котором был выполнен вызов функции для вызова **xlAutoFree** или **xlAutoFree12**. Вызов **xlAutoFree** или **xlAutoFree12** осуществляется до следующего вызова функции для этого потока. 
  
Для разработчиков, XLL существует ряд преимуществ для создания функций являющихся потокобезопасными.
  
- Они позволяют Excel, чтобы максимально эффективно использовать многопроцессорных или многоядерная компьютера.
    
- Они открываются возможность намного эффективнее, чем можно выполнить с помощью удаленных серверов с помощью одного потока.
    
Предположим, что у вас есть одним процессором компьютера, который был настроен для использования, например, *N* потоков. Предположим, что запущен электронной таблицы, что делает большое число вызовов функции XLL, в свою очередь отправляет запрос для данных или вычислений, выполняемых для удаленного сервера или кластера серверов. Может быть топологии дерева зависимостей Excel вызвать функцию N раз почти одновременно. При условии, что сервер или серверы, достаточно fast или параллельный, времени пересчета листа может добиться по мере фактор 1/N. 
  
Ключевые проблемы в создание функций потоками правильно обрабатывает конкуренции за ресурсы. Обычно это означает конфликтов памяти, и его можно разделить на две проблемы:
  
- Как создать объем памяти, вы знаете, будут использоваться только потока.
    
- Как убедиться, что к памяти с несколькими потоками безопасно.
    
В первую очередь необходимо иметь в виду — какой объем памяти в надстройке XLL доступны для всех потоков, и что доступно только из текущего потока.
  
 **Доступны для всех потоков**
  
- Переменные, структуры и экземпляры класса объявлен вне тела функции.
    
- Статические переменные, объявляемые в теле функции.
    
В этих двух случаях памяти резервируется в блоке памяти библиотеки DLL, созданные для этого экземпляра библиотеки DLL. Если другой экземпляр приложения загружает библиотеку DLL, получает собственную копию памяти, чтобы не нет конфликтов для этих ресурсов из за пределами этого экземпляра библиотеки DLL.
  
 **Доступны только для текущего потока**
  
- Автоматическое переменные в коде функции (в том числе аргументы функций).
    
В этом случае памяти резервируется в стеке для каждого экземпляра вызова функции.
  
> [!NOTE]
> Область динамически выделенной памяти зависит от области, указывающий на него указатель мыши: если указатель находится доступны для всех потоков, также является объем памяти. Если указатель находится автоматическую переменную в функцию, выделенной памяти эффективно закрытый этого потока. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Только один поток объем доступной памяти: локальной памяти потока

Учитывая, что статические переменные в теле функции будут доступны для всех потоков, функции, использующие их четко не являются потокобезопасными. Один экземпляр функции в одном потоке могут изменять значение во время другого экземпляра в другом потоке предполагается, что это совершенно другой. 
  
Существует две причины объявление статических переменных в функцию.
  
1. Статические данные сохраняются из одного вызова к следующему.
    
2. Указатель на статические данные безопасно можно получить с помощью функции.
    
В случае первая причина может потребоваться данными, сохраняет и имеет значение для всех вызовов функции: возможно простой счетчик, который увеличивается каждый раз вызывает функцию в любом потоке или структуру, которая собирает данные об использовании и производительности на ночь вызов трана. Вопрос является защита общих данных или структуру данных. Лучше всего этого с помощью критический раздел, как в следующем разделе поясняются.
  
Если данные предназначен только для использования в данный поток, который может быть установлено по причине 1 и происходит всегда по причине 2, вопрос является то, как создание объем памяти, сохраняется, но доступно только из этого потока. Одним из решений является использование локальной памяти потока (TLS) API.
  
Например рассмотрим функция, которая возвращает указатель на **структуру XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Эта функция не потокобезопасными, так как один поток может возвратить статические **XLOPER12** , в то время как другой перезаписывает ее. Вероятность такого события еще выше, если **XLOPER12** должно быть передано **xlAutoFree12**. Решением является выделить **XLOPER12**и возвращает указатель на него применить **xlAutoFree12** , чтобы освободить память **XLOPER12** . Такой подход используется в многие функции примере показано [Управление памятью в Excel](memory-management-in-excel.md).
  
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

Такой подход проще реализовать, чем подход, описанные в следующем разделе основывается на TLS API, но имеет несколько недостатков. Во-первых, Excel необходимо вызвать **xlAutoFree**/ **xlAutoFree12** любой тип возвращаемых **XLOPER**/ **XLOPER12**. Во-вторых, имеется проблема при возврате **XLOPER**/ s**XLOPER12**, которые возвращаемое значение для вызова функции обратного вызова интерфейса API для C. **XLOPER**/ **XLOPER12** могут указывать на объем памяти, который необходимо освободить путем Excel, но **XLOPER**/ **XLOPER12** самого освобождения так же, как было выполнено выделение. Если такие **XLOPER**/ **XLOPER12** — для использования в качестве возвращаемое значение функции листа XLL, невозможно просто для оповещения **xlAutoFree**/ **xlAutoFree12** требуется дополнительная обоих указатели тем способом. (Установка **xlbitXLFree** и **xlbitDLLFree** не помогает, как лечения **XLOPER/XLOPER12s** в Excel с помощью оба набора не определен и может изменяться от версии на другую.) Чтобы обойти эту проблему, XLL можно сделать глубокие копии всех выделенных Excel **XLOPER/XLOPER12s** , которая возвращает в лист. 
  
Решение, которое позволяет избежать этих ограничений для заполнения и возврата локального потока **XLOPER и XLOPER12**, подхода необходимо, **xlAutoFree/xlAutoFree12** без использования сам указатель **XLOPER и XLOPER12** . 
  
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

Следующий вопрос является, как настраивать и извлекать локальную память потока, иными словами, как реализовать функцию **get_thread_local_xloper12** в предыдущем примере. Это делается с помощью потока локального хранилища (TLS) API. Сначала необходимо получить индекс TLS с помощью **TlsAlloc**, который в конечном счете освобождается с помощью **TlsFree**. Как лучше всего выполняются из **DllMain**.
  
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

После получения индекса, следующим шагом является выделить блок памяти для каждого потока. [Документация по разработке Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) рекомендуется выполнять это каждый раз **DllMain** функции обратного вызова вызывается с **DLL_THREAD_ATTACH** событий и освобождения памяти на каждом **DLL_THREAD_DETACH**. Тем не менее выполнив этот совет вызовет библиотеки DLL выполнить ненужных рабочих потоков, не используется для пересчета. 
  
Вместо этого лучше использовать стратегию распределения на первом использовании. Во-первых необходимо определить структуру, который вы хотите выделить для каждого потока. Предыдущие примеры, которые возвращают **XLOPERs** или **XLOPER12s**следующие достаточно, но можно создать любое структуру, которая должна удовлетворять потребностям.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Следующая функция получает указатель на локальный экземпляр потока или выделяет один, если это первый вызов.
  
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

Теперь можно увидеть способ получения памяти **XLOPER и XLOPER12** локального потока: во-первых, получить указатель на экземпляр потока **TLS_data**, и затем возвращает указатель на **XLOPER и XLOPER12** , содержащиеся в нем, как показано ниже. 
  
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

Функции **mtr_safe_example_1** и **mtr_safe_example_2** могут быть зарегистрирована как функции листа потоками при запуске Excel. Тем не менее нельзя смешивать два подхода в один XLL. Ваше XLL можно экспортировать только один реализации **xlAutoFree** и **xlAutoFree12**и каждой стратегии памяти требуется используется другой подход. С помощью **mtr_safe_example_1**указатель, переданный **xlAutoFree/xlAutoFree12** освобождения вместе с данными ссылается на. С помощью **mtr_safe_example_2**нужно освободить только указывает на данные.
  
Windows также предоставляет функцию **GetCurrentThreadId**, который возвращает текущий поток уникальный системных идентификатор. Это обеспечивает разработчик с другим способом сделать надежных потока кода или сделать его поток поведение определенных.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Только с более одного потока объем доступной памяти: критических разделов

Следует защитить чтения/записи памяти, который может осуществляться более одного потока, с помощью критических секций. Именованные критический раздел требуются для каждого блока памяти, который необходимо защитить. Можно инициализировать ходе вызова функции **xlAutoOpen** и освобождать их и присвойте их значения NULL во время вызова функции **xlAutoClose** . Вы должны содержать каждого доступ в защищенный блок в паре вызовы **EnterCriticalSection** и **LeaveCriticalSection**. В разделе критические может только один поток в любое время. Ниже приведен пример инициализации, инициализации и использования секции с именем **g_csSharedTable**.
  
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

Другой, возможно, более безопасным способом защиты блока памяти является создание класса, содержащего свою собственную **CRITICAL_SECTION** и которого конструктор, деструктор и методы доступа к взяла на себя его использования. Такой подход имеет преимущество Защита объектов, которые могут быть инициализирован перед **xlAutoOpen** запускается или миру после вызова **xlAutoClose** , однако следует проявлять осторожность сведения о создании слишком много критические разделы и операционной системы Дополнительная нагрузка, при этом будет создана. 
  
При наличии кода, который требуется доступ к более одного блока защищенной памяти в то же время, необходимо тщательно рассмотрите порядок введены и выхода из критических разделов. Например следующие две функции создать взаимоблокировки.
  
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

Если первая функция в одном потоке вводит **g_csSharedTableA** , а второй — в другом потоке вводит **g_csSharedTableB**, зависание оба потока. — Это правильный подход для ввода в едином порядке и выйдите из в обратном порядке, как показано ниже.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Где это возможно, лучше с потока сотрудничестве точка зрения изоляции доступа для различных блоки, как показано ниже.
  
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

При наличии большого числа конфликтов для общего ресурса, такие как запросы часто используемые кратковременного доступа, можно использовать возможности критический раздел на вращение. Это способ, с помощью ожидание ресурса меньше процессор. Для этого можно использовать либо **InitializeCriticalSectionAndSpinCount** при инициализации раздел или **SetCriticalSectionSpinCount** после инициализации, чтобы задать число попыток потока циклически до завершения ресурсы, которые становятся доступно. Операция ожидания дорогим, поэтому прокрутка позволяет избежать таких ресурс освобождается на данном этапе. В системе одного процессора число смен хэша эффективно игнорируется, но вы по-прежнему можно указать без внесения любой вред. Диспетчер кучи памяти использует число смен хэша 4000. Дополнительные сведения об использовании критические разделы документации пакета SDK Windows. 
  
## <a name="see-also"></a>См. также



[���������� ������� � Excel](memory-management-in-excel.md)
  
[�������������� �������� � Excel](multithreaded-recalculation-in-excel.md)
  
[Диспетчер надстроек и функции XLL интерфейса](add-in-manager-and-xll-interface-functions.md)

