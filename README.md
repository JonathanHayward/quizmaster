quizmaster
==========

## README for Quizmaster 1.0b

LEGAL

    For the duration of this copyright statement, 'this software' and
    'Quizmaster' are taken to mean all original files distributed with
    this product, and the arrangement and other original work related to this
    product.

    License

        This software is copyright 2003 by Jonathan Hayward, and licensed
		and licensed to you under the your choice of the original Artistic
        License, which should be present in the file doc/artistic.txt, the
        General Public License version 2.0, which should be present in the
        file doc/gpl.txt, and the Massachusetts Institute of Technology
        License, which should be present in the file doc/mit.txt.

    Warrantee

        Jonathan Hayward makes no warranties, express or implied,
        regarding this software.  In no event shall Jonathan Hayward be
        liable for any consequential, special, incidental, or indirect
        damages of any kind arising out of the license of, use of,
        or inability to use any software or product covered under
        this license, even if Jonathan Hayward has been advised of the
        possibility of such damages.  This limitation of liability and
        risks is reflected in the price of this software.

PURPOSE

    Quizmaster is a search engine meant to provide high-usability and
    powerful access to documents being searched. It does not search the web,
    but local files provided to it. It is meant to help the user find materials
    quickly.

INSTALLATION AND SETUP

    Basics

        * To install, run "./install" and answer the questions provided.  This
          will run a Unix-flavor install-style script and should create a
          working, out-of-the-box installation when supplied appropriate
          values.

        * See USAGE below if are curions about how to use Quizmaster.

        Setup and Customization

            The Configure link at the bottom of Quizmaster search page
            provides a menu you can use to customize Quizmaster. There are some
            principles that are helpful to know.

            When you take a quiz, Quizmaster gives the results that closest
            match your answers. A quiz calculates a score based on answers to
            questions; each question (left-hand frame) has its own axis, and
            each result (right-hand frame) has a particular choice of answers
            it is closest to. (It works a bit like the Myers-Briggs Type
            Indicator.) The "parts" of a quiz are:

            The Quiz Itself
                
                You can create a new blank quiz from the Create New Quiz tab,
                under the Quizzes tab.

            Axes

                The axes for the Myers-Briggs test would be
                Extraversion-Introversion, Sensate-Intuitive, Thinking-Feeling,
                and Judging-Perceiving. You can create axes under the Axes
                tab; once you've created an axis, it is available to all
                quizzes.

            Questions

                Each question has an axis and a set of responses (ordinarily
                two responses, but you can add more). Each response has a score
                for that axis. If you were to implement the Myers-Briggs test,
                the question:

                    You feel at ease in a crowd.
                    [ ] Yes.
                    [ ] No.

                would have an axis of Extraversion-Introversion, a "Yes" would
                have a score of 1 [introverted, the first part of the axis], and
                a "No" would have a score of 10 [extraverted, the second part
                of the axis]. You can create questions, with their responses,
                from the Questions tab, under the Quizzes tab.

            Results

                Here's the one part you might not guess by trying. A result
                matches a particular set of answers; when you take a quiz, you
                get the results closest to how you answered the quiz.
                Therefore, to add results, you create a quiz with its axes and
                questions, then for each result answer the quiz in the way
                that's the result most closely matches, and click the "Add New
                Result" link at the bottom right-hand page. (You can't do this
                from the configuration window.)

            One way to develop quizzes is to figure out what basic axes (for
            instance, Conservative-Liberal) will distinguish between results,
            then add those axes, and make a quiz with questions that
            discriminate along those axes. To add a result, answer the quiz's
            questions so the result should be the #1 match, then click on "Add
            New Result".

            Confused? It sounds more confusing than it is. You know how some
            games are easy to play but impossible to figure out from someone
            reading the rules? Why don't you go through the sample quizzes, see
            how they behave, and then study them through the administrative
            interface to see how they're put together. The only really tricky
            bit is that you add a result by answering a quiz's questions for
            the way that matches the answer most quickly, then clicking on "Add
            New Result". Just try it out.

        Security

            The present release of Quizmaster has not been closely
            scrutinized for security, and should be treated as such by
            security-conscious administrators.  If you discover a
            vulnerability, please contact the author at
            jonathan.hayward@pobox.com with details.

            You are strongly encouraged to change the password in
            <the private Quizmaster data directory>/password.

            The default installation sets
            <the private Quizmaster data directory> and contents
            to a relatively permissive mode.  Administrators are encouraged to
            set directory and contents to mode 700, owned by the
            effective user ID that CGI scripts will be running under. This
            is usually apache or nobody.

USAGE

    Quizmaster is designed to be run as a straightforward web
    application, with much administrative activity performed on-web.
    Once it is set up via the Configure link, just explore.

        http://[your hostname]/cgi-bin/quizmaster

    (That is the location provided by RPM installation and the default for the
    provided installer. The provided installer allows you to specify another
    location; if you specified another location, substitute that for
    "/cgi-bin/quizmaster".)

NOTES

    Payment

        Quizmaster is linkware. It is available to you free of charge.
        If you like it, I would be very happy if you would visit
        http://JonathansCorner.com and consider linking to it.

    Bugs

        For security-related concerns, see Security above.

    Contact

        The author can be contacted at jonathan.hayward@pobox.com, and
        maintains a website at http://JonathansCorner.com. The current version
        of Quizmaster may be obtained from
        http://JonathansCorner.com/etc/quizmaster/.
