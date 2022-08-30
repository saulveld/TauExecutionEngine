# Tau Execution Engine

## Aims

To create a syntax tree that allows for a full suite of modern programming features including Image state, Object Message Handling, First Class Functions, Forced Deconstruction, Type Classes, Type Algebra, Meta Programming, IDE Application Unification, Live Coding, Just in Time Compilation the list Goes on, basically a candy store wish list of Quality of Life Software Engineering Features. Though Performance is not listed on there nor is bare metal execution.

## Ontology vs Taxonomy

Class First Programming as opposed to Object Programming tends mean creating Exhaustive Taxonomies of Classes prior to production of the minimum viable product. Object / Trait based programming tends to prefer “Operation” first programming in which the verbs are defined prior to the objects against which those verbs operate, this makes the minimum viable product easier to define and less likely to cause technical debt when designed by a less senior developer / architect.
So what is Class First Programming, that is when you define a class hierarchy prior to coding. This can also be called a prescriptive taxonomy, the problem with this is that humans are dumb and get this wrong. What is Ontology First, this tends to treat Objects as Useful Groupings of Methods without an inheritance hierarchy as the primary points of definition, so not just defining what can exist but actually creating items (Singletons) which exist on definition.

## Messages Vs Methods

What is the difference between a Method and a Message, basically the concept of Independence that a Message is a first class concept not simply a thing inside a “Class” or an “Interface”. A Message may be handled by two completely different Type Hierarchies without being a different message. This allows for Code Generators to be more powerful.

## Epistemology and Code Access and Types

Often when writing code the largest issue is the ability to access a method buried inside a private type which often requires refactoring and the use of exotic features so as to simplify the extension of functionality without violating the architectural intent. So almost always you are asking yourself the question how can this FUNCTION know this OTHER FUNCTION.

## Pure Functions Simply Associate Inputs to Outputs

All functions that is any block that returns a value if it has no variables nor calls to impure functions it can be replaced with its contents recursively and thus can be considered a synonym with a table look up.

## Data can be replaced by Pure Functions

The corollary of the Pure Functions being replaced by data is that day can always be replace by a function which obtains that value, this is the principle of lazy evaluation does not affect pure functions.

## Single Stack Resolution vs Multiple Stack Resolution

A single stack resolution means simply put a symbol is resolved to the value of a variable hosted at the nearest point on the stack and all resolution stacks that are linear with distinct symbols in each step of the resolution will have non ambiguous resolutions (will always resolve to the same easily understandable value).

## Singe Stack Return vs Multiple Stack Return

Exceptions returning in their own try catch nesting contiguously but non continuously with function scoping leads to lazy and bad code.

## Null / Nothing is a Type not a Value

Null is not a value, it’s the absence of a value in standard programming parlance however this makes no sense as it is a value as well which means that two minds must be held when dealing with a nullable type, first if it is null else what its actual value is. This kind of thinking can be removed by simply saying that null is not a value of a type but is a type of its own.

## Simplified Type Algebra and Deconstruction vs Declared Ignorance.

Because functions may need to return more than one type in different scenarios or take one or more type it means that without multiple inheritance we are stuck with duplicating methods and casting returns based on knowledge not contained in the schema of the classes. This can be avoided by allowing for “And” and “Or” compound types that allow for requiring many Type Classes or one of many Types. This means that that the function schema is descriptive of all occurrences and can also force deconstruction making sure that all consuming functions are “case complete”.

## When vs If and Case Completeness

When vs If, when is a branching in time condition, if is a universal condition. Why this matters case completeness in when groups is possible where as an if group has no concept of counterfactuals unless you nest with else but this is only capable of a defaulting classification scheme which a compiler cannot check for meaningful completeness. However a when Classification group can be invalidated at the compiler level if it is used as a Despatch Selector.

## Acidity in Code Changes

a change is not just a source code control thing its also

## Generators vs Templates vs Generics vs Macros

A Generator vs a Template or a Generic a macro is pre compilation string manipulation and a template is a more formal form of that concept, a generic is an even more regularized version limiting what can be substituted mainly only types. A Generator is something which can do everything a macro can do and a Template and a Generic because the Type System is runtime extendable. This allows for specification during execution so any valid code can construct a valid function and call it or construct a valid type and return an instance of it.

## Image vs Execution Event

A Program being a set of loaded instructions with an entry point is a very traditional view but is misleading as most applications include “Files” or stored values including configurations which affect actions on initialization. This dual nature of Traditional Programs makes the thought process around them fragmented because you have to switch between linear functionality and state based looping. Using an image instead of Traditional Instruction Set view, lets you keep the code in a more “Database” like structure and edit the code whilst running. This gives you absolute reflection powers and meta-meta programming.

## Nominal Conditional Dispatch

This is part of the when better than if concept classifications give you an ability to create value based subtypes of classes and branch on message handling despatch which simplifies the number of possible conditions in code and also cleans up the particular functions by avoiding repetitive value conditions.

## Image

## Object

## Type Rule

## Type Object

## Singleton

## Type Generator

## Cast On Pass Type

## Trait

## Or Rule

## And Rule

## Classification

## Full Classification

## Defaulted Classification

## Program

## Block

## Block Generator

## Built In

## Compound Block

## Method Definition (Named Compound Block with Known Return Type)

## Variable Definition

## Parameter Definition

## Image Layer (Middleware)

## Context

## Variable

## Expression

## Symbol Expression

## Reference Type Identity

## Primitive Identity

## Record Identity

## Call

## Order Of Resolution

## Salvation Middleware

## Compiler / Code Serializer

## Lion Compiler

## Classes and Their Required Methods

## Image Class

## Type Rule Class

## Type Object Class

list of UML DOCUMENTS

        Program
    		-> Block
    		-> BuiltIn
    		-> MethodDefintion

    	Object
    		AddVariable()
    		DefineBlock(ParamterDefintions, VariableDefinitions, Expressions);
    		DefineBlockGenerator(ParamterNames, VariableNames, ExpressionGenerators);

    	Program : Object
    		bool CanExecute(IEnumerable<Expression>);
    		bool CanExecute(IEnumerable<TypeRule>);
    		Expression Call(IEnumerable expression);
    		Block : Program
    		BlockGenerator : Program
    		CompoundBlock : Program
    		Cascade : Program, (First, AfterThat);
    		Extend(Refinement);

    		STATIC
    		Program DefineBlock(ParamterDefintions, VariableDefinitions, Expressions);
    		Program DefineBlockGenerator(ParamterNames, VariableNames, ExpressionGenerators);
    		Program DefineBuiltIn(ParameterDefintions, Func<IEnumerable<Expression>, Expression> execution);
    		Program Method(name);
    		ExtendMethod(Symbol, ProgramBeingRefined, Refinement);

    		// recursively generates the code. but if you use a generator it can only be the base call of CompoundBlock;

    	TypeRule : Object
    		Type : TypeRule
    			ImplementMethod();
    		TypeGenerator : TypeRule
    		Trait : TypeRule;
    		OrRule : TypeRule;
    		AndRule : TypeRule;

    	Image
    			LoadLayer()
    			DefineType();
    			DefineSingleton();
    			DefineTypeGenerator();
    			DefineDataType();
    			DefineTrait();
    			DefineClassifcationScheme();
    			DefineMethod(Symbol, TypeRule, BaseProgram);
    			ImplementTraitForType(Trait, Type, [(Symbol, Trait)]);
    			Program DefineBlock(ParamterDefintions, VariableDefinitions, Expressions);
    			Program DefineBlockGenerator(ParamterNames, VariableNames, ExpressionGenerators);
    			Program DefineBuiltIn(ParameterDefintions, Func<IEnumerable<Expression>, Expression> execution);
    			Program Method(name);
    			Program DefineBlock(ParamterDefintions, VariableDefinitions, Expressions);
    			Program DefineBlockGenerator(ParamterNames, VariableNames, ExpressionGenerators);
    			Program DefineBuiltIn(ParameterDefintions, Func<IEnumerable<Expression>, Expression> execution);
    			Program Method(name);
    			TypeRule Rule(name);
    			Literal(TypeRule, object);
    			Compile(string Code);

    	Compiler
    		void Compile (Image image, string code);
    		void Compile (Image image, IEnumerable<string> codes);
    		ILayer CompileLayer(IEnumerable<string> codes);

    	Serializer()
    	Salvation()

    	"FullSegmentCalssifcationScheme";
    	"PartialAndDefault";

    		Expression
    			Symbol; (Variable | Name);  -- may or may not have a known type.
    			Call;
    			Reference;

    		Expression Expression.ResolveTypes(Context);
    		Expression Expression.ResolveVariables(Context);
    		Expression Expression.ResolveCalls(Context);

    		Reorder SubBlocks
